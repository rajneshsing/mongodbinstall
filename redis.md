Question: How to install redis in wampserver?
Download the redis
   A) Download Redis setup For 32 Bit System and Install
   B) Download Redis Setup for 64 Bit system and follow below steps.    
   http://www.web-technology-experts-notes.in/2016/12/how-to-install-redis-on-wamp-server.html
Extract the zip file
Place the unzip file in c:\redis
Run redis-server.exe from c:\redis
then Run redis-cli.exe from c:\redis
Check out your php version and know whether thread safety is enabled or not(by using phpinfo()).
Now we need to download the php_redis.dll. Download the php_redis.dll from PECL.
Download as per PHP Version and thread based.
Extract the zip file.
https://pecl.php.net/package/redis/2.2.7/windows
thread safe 5.6 Thread Safe (TS) x86
php_redis-2.2.7-5.6-ts-vc11-x86.zip
Copy the php_redis.dll and paste to following folder in Wamp Server.
wamp\bin\php\php5.x.xx\ext\
Add the following line in your php.ini
extension=php_redis.dll
Re-start the wamp Server.
Do phpinfo() and search redis. It will start displaying which means its Redis is installed