
# Microproject.github.io
LINK - https://yedurunivas.github.io/Microproject.github.io/

Title of the Project : Student Enrollment Form

Description : Student Enrollment Form that will store data in STUDENT-TABLE relation of SCHOOL-DB database. Input Fields: {Roll-No, Full-Name, Class, Birth-Date, Address, Enrollment-Date}

Primary key: Roll No.

Benefits of using JsonPowerDB : Simplest way to retrieve data in a JSON format. Schema-free, Simple to use, Nimble and In-Memory database. It is built on top of one of the fastest and real-time data indexing engine - PowerIndeX. It is low level (raw) form of data and is also human readable. It helps developers in faster coding, in-turn reduces development cost. Release History (release of your JsonPowerDB related code on Github)

Additional you can have: JsonPowerDB is a Real-time, High Performance, Lightweight and Simple to Use, Rest API based Multi-mode DBMS. JsonPowerDB has ready to use API for Json document DB, RDBMS, Key-value DB, GeoSpatial DB and Time Series DB functionality. JPDB supports and advocates for true serverless and pluggable API development.

<img width="955" alt="1" src="https://github.com/YeduruNivas/Microproject.github.io/assets/96375425/520fe5f7-cf8c-4f82-be9e-73ec896d6fbb">
<img width="958" alt="2" src="https://github.com/YeduruNivas/Microproject.github.io/assets/96375425/33b4588f-0bda-4554-a95e-7b0c2314dd18">
<img width="960" alt="3" src="https://github.com/YeduruNivas/Microproject.github.io/assets/96375425/f17975ff-1b74-4b86-a7a8-eef086c866e4">
<img width="960" alt="4" src="https://github.com/YeduruNivas/Microproject.github.io/assets/96375425/bf11e03f-4912-4033-987f-2c2ce17b141d">
Scope of functionalities :

Examples of use : can be used foe various other platforms like Online Examination Registration , Job Application , profile creation , and many more other uses .

Project status : Done

Sources :Introduction to JsonPowerDB - V2.0 https://careers.login2explore.com/course/view.php?id=14

Other information Sources : https://login2explore.com/jpdb/docs.html

STEP BY STEP COURSE DOCUMENTATION :

JsonPOwerDB
Introduction to JsonPowerDB - V2.0 Login2Xplore

Creating a Developer Account and Generating Connection Token : -

Visit: http://api.login2explore.com:5577/user/index.html REGISTER After registration check your email-id for password. Login at http://api.login2explore.com:5577/user/index.html using your email and password received. First of all change password - Left Navigation >> Change Password. Login with new password.

Tools > Token > connection token > Generate (Token needed to communicate with Data Base)

90932512|-31949274757731994|90949158

Token used to execute the API

Installing Talend API Tester : -

Google > settings > Extensions > Chrome Web store > Talend API Tester - Free Edition > Add to chrome extension

Understanding JsonPowerDB and its Features : -

nimble , schema Free , simple to use , in memory and real time , easy to maintain , serverless support , enables multi mode database , power Index , Web services API Cost efficient , multiple security layers , best performance

JsonPowerDB Use case and Benefits : -

any software app that needs backend db all rdbms use cases all document db use cases all key- value db use cases use cases that needs GeoSpacial/Time series Analytics Best suited to real - time application for data analytics Improving existing application reporting/ analytics performance. Live working HTML, Templates.

PUT Command - Creating (Inserting) Record : - # IML (JPDB Index Manipulation Language) PUT : Insert single record in the database Token - 90932512|-31949274757731994|90949158

Talend > post Base url : http://api.login2explore.com:5577 End-point url : /api/iml (mentioned in command when different)

BODY : { "token": "90932512|-31949274757731994|90949158", "cmd": "PUT", "dbName": "Employee", "rel": "Emp-Rel", "jsonStr": { "id": "1", "name": "Soniya", "email": "soniya@gmail.com", "mobileno": "9967825671" } }

Send >

{"data":"{"rec_no":[1]}","additionalData":{"processReqType":0,"dbUpdateFlag":true}, "message":"RELATION CREATED, TEMPLATE CREATED FROM JSON, DATA INSERTED, Total 1 rows are inserted, Added 0 columns as New Index Columns.","status":200}

Dashboard > Visualize > Jsondb > select Database and Relation

1 2/24/2023, 8:21:16 PM soniya@gmail.com 1 9967825671 Soniya

New row -

{ "token": "90932512|-31949274757731994|90949158", "cmd": "PUT", "dbName": "Employee", "rel": "Emp-Rel", "jsonStr": { "id": "2", "name": "aniket", "email": "aniket@gmail.com", "mobileno": "8582887792" } }

{"data":"{"rec_no":[2]}","additionalData":{"processReqType":0,"dbUpdateFlag":true}, "message":"DATA INSERTED, Total 1 rows are inserted, Added 0 columns as New Index Columns.","status":200}

Dashboard > Visualize > Jsondb > select Database and Relation

1 2/24/2023, 8:21:16 PM soniya@gmail.com 1 9967825671 Soniya 2 2/24/2023, 8:24:57 PM aniket@gmail.com 2 8582887792 aniket

GET Command - Retrieving Record : - # IRL (JPDB Index Retrieval Language)

Talend - Add a project

Name - PUT Project - JPDB Service - CRUD save

GET_BY_KEY : Retrieve single record by json data

Talend > Save as > Name : GET >

POST | http://api.login2explore.com:5577/api/irl

"token": "90932512|-31949274757731994|90949158",

{ "token": "90932512|-31949274757731994|90949158", "dbName": "Employee", "cmd": "GET", "rel": "Emp-Rel", "jsonStr": { "name": "aniket" }

}

{"data" :"{"name":"aniket","id":"2","mobileno":"8582887792","email":"aniket@gmail.com"}" ,"message":"DATA RETRIEVED FROM PI","status":200}

UPDATE Command - Update a record : - # IML (JPDB Index Manipulation Language)

UPDATE : Update multiple records in the database or add a new column in a record

POST | http://api.login2explore.com:5577/api/iml

{ "token": "90932512|-31949274757731994|90949158", "dbName": "Employee", "cmd": "UPDATE", "rel": "Emp-Rel", "jsonStr": { "1" : { "name": "raju", "email" : "raju@gmail.com" } "2" : { "mobileno":"66666666" } }

}

{"data":"{"1":{"name":"Soniya","email":"soniya@gmail.com"},"2": {"mobileno":"8582887792"},"NewIndexColumnCreated":0,"NewNonIndexColumnCreated":0}","additionalData": {"processReqType":0,"dbUpdateFlag":true},"message":"Success","status":200}
REMOVE Command - Remove a record : - # IML (JPDB Index Manipulation Language) - To insert, update and delete Json data.

REMOVE : Remove records from the database

POST | http://api.login2explore.com:5577/api/iml

{ "token": "90932512|-31949274757731994|90949158", "dbName": "Employee", "cmd": "REMOVE", "rel": "Emp-Rel", "record" : 1

}

{"data":"{"removedRecNos":[1],"alreadyRemovedRecNos":[],"invalidRecNos":[]}","additionalData": {"processReqType":0,"dbUpdateFlag":true},"message":"Success","status":200}

2 2/24/2023, 8:24:57 PM aniket@gmail.com 2 66666666 aniket

Test - Understanding JPDB

Test your knowledge

Attempts allowed: 5

Time limit: 5 mins

Grading method: Highest grade

Summary of your previous attempts Attempt State Grade / 5.00 Review Feedback 1 Finished Submitted Friday, 24 February 2023, 9:20 PM 5.00 Congratulations!! Excellent Performance! Keep it Up.

Highest grade: 5.00 / 5.00. Overall feedback Congratulations!! Excellent Performance! Keep it Up.
Ajax Concepts - A Desktop application feel on web-pages ; -

AJAX - Asynchronous JavaScript And XML.
How to use JsonPowerDB in Web Pages

https://drive.google.com/file/d/1e4VN4PAec-Y1iFsj0BN5j0pM7mfed0VQ/view?usp=sharing


