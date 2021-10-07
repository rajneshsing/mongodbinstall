download mongodb and place inside mongodb folder
then php_mongo.dll for same version in ext folder
add php.ini 
extension=php_mongo.dll;
C:\>md \data\db
and then
C:\>C:\MongoDB\bin\mongod.exe
then open new window and type 
C:\Users\Pankaj>C:\MongoDB\bin\mongo.exe

C:\mongodb\bin>mongodump --db testdb --out c:\TEMP\op.json   Ok create metadata
C:\mongodb\bin>mongorestore -d chkdb c:\TEMP\op.json\chkdb   ok for all table
C:\mongodb\bin>mongoexport --db testdb --collection users --out c:\Users\CEINFO\users.json ok  single table



mongodump --host xx.xxx.xx.xx --port 27017 --db your_db_name --username your_user_name --password your_password --out /target/folder/path

C:\mongodb\bin>mongoimport --db testdb --file c:\Users\CEINFO\users.json 

C:\mongodb\bin>mongoimport --db testdb --collection jazz --file c:\Users\CEINFO\users.json single table

https://www.quackit.com/mongodb/tutorial/mongodb_import_data.cfm