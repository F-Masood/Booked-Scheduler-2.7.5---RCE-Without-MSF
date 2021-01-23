# Booked Scheduler 2.7.5 - Remote Command Execution Without Metasploit
##### Dated: 23 Jan 2021 - Author: F-Masood
##### Description: This is a manual way (without using metasploit) of exploiting the **CVE 2019-9581** or **EDB-ID:46486** vulnerablity. 
Please note the orignal credit of finding this vulnerability goes to AKKUS ---> https://www.exploit-db.com/?author=9483. \
The vulnerablity requires authenticated user (admin login) as a pre-req. After logging as ADMIN, the user can upload a malicious php script by exploiting arbitrary file upload vulnerability in ico file upload section. 

##### PoC

1. Login to the Booked Scheduler 2.7.5 web portal.
![alt text](https://github.com/F-Masood/Booked-Scheduler-2.7.5---RCE-Without-MSF/blob/main/01.png)
