nsa-header
==========

Adds a NSA friendly copyright license HTTP header to popular webservers.

* [EFF: NSA Spying](https://www.eff.org/nsa-spying)

Fun Idea From: [aestetix](http://aestetix.com/2013/07/11/fighting-back-against-the-nsa-with-http/)


Webservers
------------------
* Apache
* Nginx


Testing The Header
------------------

Test our your new header is easy enough.
`curl --head www.example.com 2>&1  | grep :`

    $ curl --head www.example.com 2>&1  | grep :
    0   162    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0
    Server: nginx
    Date: Thu, 11 Jul 2013 23:58:05 GMT
    Content-Type: text/html; charset=utf-8
    Content-Length: 162
    Location: http://www.example.com/
    Connection: keep-alive
    X_FUCK_THE_NSA: This copyright notice entitles me to receive a copy of all requests stored on demand. If you choose not to accept this license, your only recourse is to delete all stored requests with this signature. This notice shall also serve as my written submission for all copies of all stored requests.
    Expires: Thu, 25 Jul 2013 23:58:05 GMT
    Cache-Control: max-age=1209600
    Strict-Transport-Security: max-age=31536000

