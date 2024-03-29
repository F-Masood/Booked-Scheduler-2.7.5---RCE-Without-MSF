# Booked Scheduler 2.7.5 - Remote Command Execution Without Metasploit
##### Dated: 23 Jan 2021 - Author: F-Masood
##### Description: This is a manual way (without using metasploit) of exploiting the **CVE 2019-9581** or **EDB-ID:46486** vulnerablity.
##### Need: Just to avoid using MSF, I made this one ;-) 

Please note the original  credit of finding this vulnerability goes to AKKUS ---> https://www.exploit-db.com/?author=9483. \
The vulnerability requires authenticated user (admin login) as a pre-req. After logging as ADMIN, the user can upload a malicious php script by exploiting arbitrary file upload vulnerability in ico file upload section. 

##### PoC

1. Login to the Booked Scheduler 2.7.5 web portal.
![alt text](https://github.com/F-Masood/Booked-Scheduler-2.7.5---RCE-Without-MSF/blob/main/01.png)

2. Navigate to manage_theme.php page. 
![alt text](https://github.com/F-Masood/Booked-Scheduler-2.7.5---RCE-Without-MSF/blob/main/02.png)

3. Under **Favicon** section, upload your malicious **php** script e.g. I am uploading a file **rce.php** Also, I am using Burp to intercept my request, although Burp part is not necessary.
![alt text](https://github.com/F-Masood/Booked-Scheduler-2.7.5---RCE-Without-MSF/blob/main/03.png)

4. The file is ready to be uploaded. The highlighted section shows the contents of codeexec.php. You can grab this **codeexec.php** from here -> https://raw.githubusercontent.com/F-Masood/php-backdoors/main/rce.php
![alt text](https://github.com/F-Masood/Booked-Scheduler-2.7.5---RCE-Without-MSF/blob/main/04.png)

5. Navigate to **custom-favicon.php** file, give some command as input and you have achieved **RCE**. Wohoooo!!!
![alt text](https://github.com/F-Masood/Booked-Scheduler-2.7.5---RCE-Without-MSF/blob/main/05.png)
