### Cassios Proving Ground Practice

### Difficulty = Hard

### IP Address = 192.168.88.116

Nmap Scan:

```
┌──(mark__haxor)-[~/_/B2B/Pg/Practice/Cassios]                                                                                                                                                              [91/92]
└─$ nmap -sCV -A 192.168.88.116 -p22,80,139,445,8080 -oN nmapscan                                                                                                                                                  
Starting Nmap 7.92 ( https://nmap.org ) at 2023-01-22 04:41 WAT                                                                                                                                                    
Nmap scan report for 192.168.88.116                                                                                                                                                                                
Host is up (0.22s latency).                                                                                                                                                                                        
                                                                                                                                                                                                                   
PORT     STATE SERVICE     VERSION                                                                                                                                                                                 
22/tcp   open  ssh         OpenSSH 7.4 (protocol 2.0)                                                                                                                                                              
| ssh-hostkey:                                                                                                                                                                                                     
|   2048 36:cd:06:f8:11:72:6b:29:d8:d8:86:99:00:6b:1d:3a (RSA)                                                                                                                                                     
|   256 7d:12:27:de:dd:4e:8e:88:48:ef:e3:e0:b2:13:42:a1 (ECDSA)                                                                                                                                                    
|_  256 c4:db:d3:61:af:85:95:0e:59:77:c5:9e:07:0b:2f:74 (ED25519)                                                                                                                                                  
80/tcp   open  http        Apache httpd 2.4.6 ((CentOS))                                                                                                                                                           
|_http-title: Landed by HTML5 UP                                                                                                                                                                                   
| http-methods:                                                                                                                                                                                                    
|_  Potentially risky methods: TRACE                                                                                                                                                                               
|_http-server-header: Apache/2.4.6 (CentOS)                                                                                                                                                                        
139/tcp  open  netbios-ssn Samba smbd 3.X - 4.X (workgroup: SAMBA)                                                                                                                                                 
445/tcp  open  netbios-ssn Samba smbd 4.10.4 (workgroup: SAMBA)                                                                                                                                                    
8080/tcp open  http-proxy                                                                                                                                                                                          
| fingerprint-strings:                                                                                                                                                                                             
|   GetRequest:                                                                                                                                                                                                    
|     HTTP/1.1 200                                                                                                                                                                                                 
|     X-Content-Type-Options: nosniff                                                                                                                                                                              
|     X-XSS-Protection: 1; mode=block                                                                                                                                                                              
|     Cache-Control: no-cache, no-store, max-age=0, must-revalidate                                                                                                                                                
|     Pragma: no-cache                                                                                                                                                                                             
|     Expires: 0                                                                                                                                                                                                   
|     X-Frame-Options: DENY                                                                                                                                                                                        
|     Content-Type: text/html;charset=UTF-8                                                                                                                                                                        
|     Content-Language: en-US                                                                                                                                                                                      
|     Date: Sun, 22 Jan 2023 03:42:05 GMT                                                                                                                                                                          
|     Connection: close                                                                                                                                                                                            
|     <!doctype html>                                                                                                                                                                                              
|     <html lang="en">                                                                                                                                                                                             
|     <head>                                                                                                                                                                                                       
|     <meta charset="utf-8">                                                                                                                                                                                       
|     <meta http-equiv="x-ua-compatible" content="ie=edge">                                                                                                                                                        
|     <meta name="viewport" content="width=device-width, initial-scale=1">                                                                                                                                         
|     <title></title>                                                                                                                                                                                              
|     <link rel="stylesheet" href="/css/main.css">                                                                                                                                                                 
|     </head>                                                                                                                                                                                                      
|     <body>                                                                                                                                                                                                       
|     <div class="small-container">                                                                                                                                                                                
|     <div class="flex-row">                                                                                                                                                                                       
|     <h1>Recycler Management System</h1>                                                                                                                                                                          
|     </div>                                                                                                                                                                                                       
|     <div class="flex-row">                                                                                                                                                                                       
|     <img src="/images/factory.jpg" class="round-button">                                                                                                                                                         
|     </div>                                                                                                                                                                                                       
|     </div>                                                                                                                                                                                                       
|     <br>                                                                                                                                                                                                         
|     <div class="small-container">
|     <div class="small-container">
|     <div class="flex-small">Control system for the factory
|   HTTPOptions: 
|     HTTP/1.1 200 
|     Allow: GET,HEAD,OPTIONS
|     X-Content-Type-Options: nosniff
|     X-XSS-Protection: 1; mode=block
|     Cache-Control: no-cache, no-store, max-age=0, must-revalidate
|     Pragma: no-cache
|     Expires: 0
|     X-Frame-Options: DENY
|     Content-Length: 0
|     Date: Sun, 22 Jan 2023 03:42:05 GMT
|     Connection: close
|   RTSPRequest: 
|     HTTP/1.1 400 
|     Content-Type: text/html;charset=utf-8
|     Content-Language: en
|     Content-Length: 435
|     Date: Sun, 22 Jan 2023 03:42:05 GMT
|     Connection: close
|     <!doctype html><html lang="en"><head><title>HTTP Status 400 
|     Request</title><style type="text/css">body {font-family:Tahoma,Arial,sans-serif;} h1, h2, h3, b {color:white;background-color:#525D76;} h1 {font-size:22px;} h2 {font-size:16px;} h3 {font-size:14px;} p {fon
t-size:12px;} a {color:black;} .line {height:1px;background-color:#525D76;border:none;}</style></head><body><h1>HTTP Status 400 
|_    Request</h1></body></html>
|_http-title: Site doesn't have a title (text/html;charset=UTF-8).
|_http-trane-info: Problem with XML parsing of /evox/about
|_http-open-proxy: Proxy might be redirecting requests
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port8080-TCP:V=7.92%I=7%D=1/22%Time=63CCB08D%P=x86_64-pc-linux-gnu%r(Ge
SF:tRequest,429,"HTTP/1\.1\x20200\x20\r\nX-Content-Type-Options:\x20nosnif
SF:f\r\nX-XSS-Protection:\x201;\x20mode=block\r\nCache-Control:\x20no-cach
SF:e,\x20no-store,\x20max-age=0,\x20must-revalidate\r\nPragma:\x20no-cache
SF:\r\nExpires:\x200\r\nX-Frame-Options:\x20DENY\r\nContent-Type:\x20text/
SF:html;charset=UTF-8\r\nContent-Language:\x20en-US\r\nDate:\x20Sun,\x2022
SF:\x20Jan\x202023\x2003:42:05\x20GMT\r\nConnection:\x20close\r\n\r\n<!doc
SF:type\x20html>\n<html\x20lang=\"en\">\n\n<head>\n\x20\x20<meta\x20charse
SF:t=\"utf-8\">\n\x20\x20<meta\x20http-equiv=\"x-ua-compatible\"\x20conten
SF:t=\"ie=edge\">\n\x20\x20<meta\x20name=\"viewport\"\x20content=\"width=d
SF:evice-width,\x20initial-scale=1\">\n\n\x20\x20<title></title>\n\n\x20\x
SF:20<link\x20rel=\"stylesheet\"\x20href=\"/css/main\.css\">\n\x20\x20\n</
SF:head>\n\n<body>\n\t\n\t<div\x20class=\"small-container\">\n\t\t<div\x20
SF:class=\"flex-row\">\n\t\t\t<h1>Recycler\x20Management\x20System</h1>\n\
SF:t\t</div>\n\t\t<div\x20class=\"flex-row\">\n\t\t\t<img\x20src=\"/images
SF:/factory\.jpg\"\x20class=\"round-button\">\n\t\t</div>\x20\n\n\t</div>\
SF:n\t<br>\n\t<div\x20class=\"small-container\">\n\n\t\t\t<div\x20class=\"
SF:flex-small\">Control\x20system\x20for\x20the\x20factory\x20")%r(HTTPOpt
SF:ions,12B,"HTTP/1\.1\x20200\x20\r\nAllow:\x20GET,HEAD,OPTIONS\r\nX-Conte
SF:nt-Type-Options:\x20nosniff\r\nX-XSS-Protection:\x201;\x20mode=block\r\
SF:nCache-Control:\x20no-cache,\x20no-store,\x20max-age=0,\x20must-revalid
SF:ate\r\nPragma:\x20no-cache\r\nExpires:\x200\r\nX-Frame-Options:\x20DENY
SF:\r\nContent-Length:\x200\r\nDate:\x20Sun,\x2022\x20Jan\x202023\x2003:42
SF:/factory\.jpg\"\x20class=\"round-button\">\n\t\t</div>\x20\n\n\t</div>\
SF:n\t<br>\n\t<div\x20class=\"small-container\">\n\n\t\t\t<div\x20class=\"
SF:flex-small\">Control\x20system\x20for\x20the\x20factory\x20")%r(HTTPOpt
SF:ions,12B,"HTTP/1\.1\x20200\x20\r\nAllow:\x20GET,HEAD,OPTIONS\r\nX-Conte
SF:nt-Type-Options:\x20nosniff\r\nX-XSS-Protection:\x201;\x20mode=block\r\
SF:nCache-Control:\x20no-cache,\x20no-store,\x20max-age=0,\x20must-revalid
SF:ate\r\nPragma:\x20no-cache\r\nExpires:\x200\r\nX-Frame-Options:\x20DENY
SF:\r\nContent-Length:\x200\r\nDate:\x20Sun,\x2022\x20Jan\x202023\x2003:42
SF::05\x20GMT\r\nConnection:\x20close\r\n\r\n")%r(RTSPRequest,24E,"HTTP/1\
SF:.1\x20400\x20\r\nContent-Type:\x20text/html;charset=utf-8\r\nContent-La
SF:nguage:\x20en\r\nContent-Length:\x20435\r\nDate:\x20Sun,\x2022\x20Jan\x
SF:202023\x2003:42:05\x20GMT\r\nConnection:\x20close\r\n\r\n<!doctype\x20h
SF:tml><html\x20lang=\"en\"><head><title>HTTP\x20Status\x20400\x20\xe2\x80
SF:\x93\x20Bad\x20Request</title><style\x20type=\"text/css\">body\x20{font
SF:-family:Tahoma,Arial,sans-serif;}\x20h1,\x20h2,\x20h3,\x20b\x20{color:w
SF:hite;background-color:#525D76;}\x20h1\x20{font-size:22px;}\x20h2\x20{fo
SF:nt-size:16px;}\x20h3\x20{font-size:14px;}\x20p\x20{font-size:12px;}\x20
SF:a\x20{color:black;}\x20\.line\x20{height:1px;background-color:#525D76;b
SF:order:none;}</style></head><body><h1>HTTP\x20Status\x20400\x20\xe2\x80\
SF:x93\x20Bad\x20Request</h1></body></html>");
Service Info: Host: CASSIOS

Host script results:
| smb-security-mode: 
|   account_used: <blank>
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
| smb2-time: 
|   date: 2023-01-22T03:42:25
|_  start_date: N/A
| smb2-security-mode: 
|   3.1.1: 
|_    Message signing enabled but not required
| smb-os-discovery: 
|   OS: Windows 6.1 (Samba 4.10.4)
|   Computer name: cassios
|   NetBIOS computer name: CASSIOS\x00
|   Domain name: \x00
|   FQDN: cassios
|_  System time: 2023-01-21T22:42:24-05:00
|_clock-skew: mean: 1h39m59s, deviation: 2h53m12s, median: 0s

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 36.71 seconds
```

Checking smb 

```
┌──(mark__haxor)-[~/_/B2B/Pg/Practice/Cassios]
└─$ smbclient -L 192.168.88.116                                                    
Password for [WORKGROUP\mark]:
Anonymous login successful

        Sharename       Type      Comment
        ---------       ----      -------
        print$          Disk      Printer Drivers
        Samantha Konstan Disk      Backups and Recycler files
        IPC$            IPC       IPC Service (Samba 4.10.4)
Reconnecting with SMB1 for workgroup listing.
Anonymous login successful

        Server               Comment
        ---------            -------

        Workgroup            Master
        ---------            -------
```

Connecting to the share and accessing files in it

```
┌──(mark__haxor)-[~/_/B2B/Pg/Practice/Cassios]
└─$ smbclient '//192.168.88.116/Samantha Konstan'
Password for [WORKGROUP\mark]:
Anonymous login successful
Try "help" to get a list of possible commands.
smb: \> ls
  .                                   D        0  Thu Oct  1 21:28:46 2020
  ..                                  D        0  Thu Sep 24 18:38:10 2020
  recycler.ser                        N        0  Thu Sep 24 02:35:15 2020
  readme.txt                          N      478  Thu Sep 24 18:32:50 2020
  spring-mvc-quickstart-archetype      D        0  Thu Sep 24 18:36:11 2020
  thymeleafexamples-layouts           D        0  Thu Sep 24 18:37:09 2020
  resources.html                      N    42713  Thu Sep 24 18:37:41 2020
  pom-bak.xml                         N     2187  Thu Oct  1 21:28:46 2020

                8374272 blocks of size 1024. 6448968 blocks available
smb: \> cd spring-mvc-quickstart-archetype\
smb: \spring-mvc-quickstart-archetype\> ls
  .                                   D        0  Thu Sep 24 18:36:11 2020
  ..                                  D        0  Thu Oct  1 21:28:46 2020
  README.md                           N     4778  Thu Sep 24 18:35:01 2020
  archetype-catalog.xml               N      774  Thu Sep 24 18:35:01 2020
  src                                 D        0  Thu Sep 24 18:35:01 2020
  pom.xml                             N     1732  Thu Sep 24 18:36:11 2020

                8374272 blocks of size 1024. 6448968 blocks available
smb: \spring-mvc-quickstart-archetype\> 

```

There are lots of files in it 

So i can either mount it on my device and view them or i can just get them all 

Let me get them all using smbget tool

```
┌──(mark__haxor)-[~/_/Pg/Practice/Cassios/smb]                                                                                                                                                                     
└─$ smbget -U anonymous -R 'smb://192.168.88.116/Samantha Konstan'                                                                                                                                                 
Password for [anonymous] connecting to //192.168.88.116/Samantha Konstan:                                                                                                                                          
Using workgroup WORKGROUP, user anonymous
smb://192.168.88.116/Samantha Konstan/recycler.ser  
smb://192.168.88.116/Samantha Konstan/readme.txt    
smb://192.168.88.116/Samantha Konstan/spring-mvc-quickstart-archetype/README.md                          
smb://192.168.88.116/Samantha Konstan/spring-mvc-quickstart-archetype/archetype-catalog.xml              
smb://192.168.88.116/Samantha Konstan/spring-mvc-quickstart-archetype/src/main/resources/META-INF/maven/archetype-metadata.xml                                                                                     
smb://192.168.88.116/Samantha Konstan/spring-mvc-quickstart-archetype/src/main/resources/archetype-resources/.gitignore                                                                                            
smb://192.168.88.116/Samantha Konstan/spring-mvc-quickstart-archetype/src/main/resources/archetype-resources/pom.xml                                                                                               
smb://192.168.88.116/Samantha Konstan/spring-mvc-quickstart-archetype/src/main/resources/archetype-resources/src/main/java/Application.java                                                                        
smb://192.168.88.116/Samantha Konstan/spring-mvc-quickstart-archetype/src/main/resources/archetype-resources/src/main/java/account/Account.java                                                                    
smb://192.168.88.116/Samantha Konstan/spring-mvc-quickstart-archetype/src/main/resources/archetype-resources/src/main/java/account/AccountController.java                                                          
smb://192.168.88.116/Samantha Konstan/spring-mvc-quickstart-archetype/src/main/resources/archetype-resources/src/main/java/account/AccountRepository.java                                                          
[---------------------------------------------------------------SNIP------------------------------------------------------------------------------]                                                         
smb://192.168.88.116/Samantha Konstan/spring-mvc-quickstart-archetype/src/main/resources/archetype-resources/src/main/resources/logback.xml                                                                        
smb://192.168.88.116/Samantha Konstan/spring-mvc-quickstart-archetype/src/main/resources/archetype-resources/src/main/resources/persistence-pgsql.properties                                                       
smb://192.168.88.116/Samantha Konstan/spring-mvc-quickstart-archetype/src/main/resources/archetype-resources/src/main/resources/persistence.properties                                                             
smb://192.168.88.116/Samantha Konstan/spring-mvc-quickstart-archetype/src/main/resources/archetype-resources/src/main/webapp/WEB-INF/i18n/messages.properties                                                      
smb://192.168.88.116/Samantha Konstan/spring-mvc-quickstart-archetype/src/main/resources/archetype-resources/src/main/webapp/WEB-INF/views/error/general.html                                                      
smb://192.168.88.116/Samantha Konstan/spring-mvc-quickstart-archetype/src/main/resources/archetype-resources/src/main/webapp/WEB-INF/views/fragments/components.html                                               
smb://192.168.88.116/Samantha Konstan/spring-mvc-quickstart-archetype/src/main/resources/archetype-resources/src/main/webapp/WEB-INF/views/fragments/layout.html        
````

Lots of file in smb 

Well i think its because thats likely the web source code 🤔

Anyways fuzzing for directories on port 80

```
                                                                                                                                                                                                                  
┌──(mark__haxor)-[~/_/B2B/Pg/Practice/Cassios]
└─$ gobuster dir -u http://192.168.88.116/ -w /usr/share/wordlists/dirb/common.txt -t64                                                        
===============================================================
Gobuster v3.2.0-dev
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://192.168.88.116/
[+] Method:                  GET
[+] Threads:                 64
[+] Wordlist:                /usr/share/wordlists/dirb/common.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.2.0-dev
[+] Timeout:                 10s
===============================================================
2023/01/22 05:09:22 Starting gobuster in directory enumeration mode
===============================================================
/.hta                 (Status: 403) [Size: 206]
/.htpasswd            (Status: 403) [Size: 211]
/.htaccess            (Status: 403) [Size: 211]
/assets               (Status: 301) [Size: 237] [--> http://192.168.88.116/assets/]
/backup_migrate       (Status: 301) [Size: 245] [--> http://192.168.88.116/backup_migrate/]
/cgi-bin/             (Status: 403) [Size: 210]
/images               (Status: 301) [Size: 237] [--> http://192.168.88.116/images/]
/index.html           (Status: 200) [Size: 9088]
/download             (Status: 200) [Size: 1479862]
Progress: 4614 / 4615 (99.98%)===============================================================
2023/01/22 05:09:46 Finished
===============================================================
```

backup_migrate looks interesting

Checking it out
![image](https://user-images.githubusercontent.com/113513376/213900220-30283c84-7b48-4f3f-81b4-be18baeb9436.png)

Hmmm recycle.tar lets download it and see its content

```
                                                                                                                                                                                                            [45/45]
┌──(mark__haxor)-[~/_/B2B/Pg/Practice/Cassios]                                                                                                                                                                     
└─$ mv ~/Downloads/recycler.tar .                                                                                                                                                                                  
                                                                                                                                                                                                                   
┌──(mark__haxor)-[~/_/B2B/Pg/Practice/Cassios]                                                                                                                                                                     
└─$ tar -xf recycler.tar                                                                                                                                                                                           
                                                                                                                                                                                                                   
┌──(mark__haxor)-[~/_/B2B/Pg/Practice/Cassios]                                                                                                                                                                     
└─$ l                                                                                                                                                                                                              
nmapscan  recycler.tar  smb/  src/                                                                                                                                                                                 
                                                                                                                                                                                                                   
┌──(mark__haxor)-[~/_/B2B/Pg/Practice/Cassios]                                                                                                                                                                     
└─$ cd src                                                                                                                                                                                                         
                                                                                                                                                                                                                   
┌──(mark__haxor)-[~/_/Pg/Practice/Cassios/src]                                                                                                                                                                     
└─$ l                                                                                                                                                                                                              
main/          
┌──(mark__haxor)-[~/_/Pg/Practice/Cassios/src]                                                                                                                                                                     
└─$ cd main/java/com/industrial/recycler                                                                                                                                                                           
                                                                                                                                                                                                                   
┌──(mark__haxor)-[~/_/java/com/industrial/recycler]
└─$ l
DashboardController.java  MvcConfig.java  RecyclerApplication.java  Recycler.java  Test.java  WebSecurityConfig.java

┌──(mark__haxor)-[~/_/java/com/industrial/recycler]
└─$ cat WebSecurityConfig.java                    
package com.industrial.recycler;

import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import org.springframework.security.config.annotation.web.builders.HttpSecurity;
import org.springframework.security.config.annotation.web.configuration.EnableWebSecurity;
import org.springframework.security.config.annotation.web.configuration.WebSecurityConfigurerAdapter;
import org.springframework.security.core.userdetails.User;
import org.springframework.security.core.userdetails.UserDetails;
import org.springframework.security.core.userdetails.UserDetailsService;
import org.springframework.security.provisioning.InMemoryUserDetailsManager;

@Configuration
@EnableWebSecurity
public class WebSecurityConfig extends WebSecurityConfigurerAdapter {
        @Override
        protected void configure(HttpSecurity http) throws Exception {
                http
                        .authorizeRequests()
                                .antMatchers("/", "/home", "/js/**", "/css/**", "/images/**").permitAll() 
                                .anyRequest().authenticated()
                                .and()
                        .formLogin()
                                .loginPage("/login") 
                                .permitAll()
                                .and()
                        .logout()
                                .permitAll();
        }

        @Bean
        @Override
        public UserDetailsService userDetailsService() {
                UserDetails user =
                         User.withDefaultPasswordEncoder()
                                .username("recycler")
                                .password("DoNotMessWithTheRecycler123")
                                .roles("USER")
                                .build();

                return new InMemoryUserDetailsManager(user);
        }
}                                                   
```

We have a cred in the file `recycler:DoNotMessWithTheRecycler123`

Lets check port 8080 and see whats in it

We're greeted with a login page
![image](https://user-images.githubusercontent.com/113513376/213900372-c1d582ce-dcbf-43ef-869d-f61a79d1a7e0.png)

Trying the cred gotten from the recyler.tar file works
![image](https://user-images.githubusercontent.com/113513376/213900391-9ce5fffc-d5af-4ace-ac71-39df74b84e91.png)

Now it have few functions lets check out what they do

NOthing really much the check status just checks status

But since we have the source code lets check it out

Now we see that the checkstatus calls on a recycler.ser file from the users backup folder
![image](https://user-images.githubusercontent.com/113513376/213900488-6fe51f73-b95e-42d5-b3ce-ea98232d8bac.png)

Now now we totally have access over that folder cause its the same as the folger in smb

```
┌──(mark__haxor)-[~/_/B2B/Pg/Practice/Cassios]
└─$ smbclient '//192.168.88.116/Samantha Konstan'                  
Password for [WORKGROUP\mark]:
Anonymous login successful
Try "help" to get a list of possible commands.
smb: \> ls
  .                                   D        0  Thu Oct  1 21:28:46 2020
  ..                                  D        0  Thu Sep 24 18:38:10 2020
  recycler.ser                        N      144  Sun Jan 22 05:18:44 2023
  readme.txt                          N      478  Thu Sep 24 18:32:50 2020
  spring-mvc-quickstart-archetype      D        0  Thu Sep 24 18:36:11 2020
  thymeleafexamples-layouts           D        0  Thu Sep 24 18:37:09 2020
  resources.html                      N    42713  Thu Sep 24 18:37:41 2020
  pom-bak.xml                         N     2187  Thu Oct  1 21:28:46 2020

                8374272 blocks of size 1024. 6447356 blocks available
smb: \> 
```

Now i also noticed it uses readObject() function which is vulnerable to deserilization 

So this is an insecure deserilization attack

Lets create the payload then xD







                                             


