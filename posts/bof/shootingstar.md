<h3> Shooting Star HackTheBox </h3>

#### Basic File Checks
![image](https://user-images.githubusercontent.com/113513376/222980704-b15aee2b-5628-4df9-9a4a-bcecf033f4fb.png)

We're working with a x64 binary which is not stripped and it has only NX enabled as its protection

I'll run it to know what it does
![image](https://user-images.githubusercontent.com/113513376/222980846-a822afc4-927c-4ee2-89e3-3b69238e166f.png)

Using ghidra i'll decompile the binary

Here's the main function
![image](https://user-images.githubusercontent.com/113513376/222980933-c5983abb-50d8-4c67-97de-b179c2892bc1.png)

It just calls the write() function which will just put the banner of the program

And it calls the star() function

Here's the decompiled star() function
![image](https://user-images.githubusercontent.com/113513376/222981313-e4f10b47-00f1-4679-8485-fbf4b0f13fc5.png)

```
void star(void)

{
  char option [2];
  undefined buffer [64];
  
  read(0,option,2);
  if (option[0] == '1') {
    write(1,&DAT_00402008,3);
    read(0,buffer,0x200);
    write(1,"\nMay your wish come true!\n",0x1a);
  }
  else if (option[0] == '2') {
    write(1,"Isn\'t the sky amazing?!\n",0x18);
  }
  else if (option[0] == '3') {
    write(1,
          "A star is an astronomical object consisting of a luminous spheroid of plasma held togethe r by its own gravity. The nearest star to Earth is the Sun. Many other stars are visible t o the naked eye from Earth during the night, appearing as a multitude of fixed luminous po ints in the sky due to their immense distance from Earth. Historically, the most prominent  stars were grouped into constellations and asterisms, the brightest of which gained prope r names. Astronomers have assembled star catalogues that identify the known stars and prov ide standardized stellar designations.\n"
          ,0x242);
  }
  return;
```

We can tell what it does:

```
1. Checks if our input option is 1, if its that we get a read syscall which reads in 0x200 bytes and store in a 64 byte buffer # bug here
2. If option chosen is 2 it prints our isn't the sky amazing
3. If option is 3 it prints out that large text
```

Our vulnerability lays in the first option since we allowed to give an input which the size allocated to us ix 0x200 bytes whereas the buffer can only hold up 64 bytes of data

We can confirm the buffer overflwo by putting long A's 
![image](https://user-images.githubusercontent.com/113513376/222981958-cad8501f-f3ab-4065-a5d5-adf1869aff0f.png)

Cool so lets get the offset 
![image](https://user-images.githubusercontent.com/113513376/222982035-7d099617-69da-4fd6-964c-d7f2361a5ef4.png)
![image](https://user-images.githubusercontent.com/113513376/222982040-c19d1090-e7fe-4887-8bb9-660c3263d059.png)

The offset is 72

But now how to we get shell?

During the program execution write got is already populated
![image](https://user-images.githubusercontent.com/113513376/222982323-d937e0e8-179c-4fc2-8bb3-209ff0babe3a.png)
![image](https://user-images.githubusercontent.com/113513376/222982336-a91123fa-e5fc-4ceb-9638-60a78a52d5db.png)

So the best thing at this point is to perform a Ret2Libc attack

