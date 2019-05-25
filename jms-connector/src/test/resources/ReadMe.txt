This application required to use ActiveMQ 5.15.9 version to use because jar file are used of this version only.
We can use another version but we have to remove complete jar(except ojdbc6.jar) and paster specific version related jars.
----------------------------------------------

Queue Name: Salim
Topic Name: Sonu
--------Request payload-------------------
POST /activemq/publish HTTP/1.1
Host: localhost:8081
Cache-Control: no-cache
Postman-Token: ddb3be62-957e-0b0c-ebf1-c62df73cbe25

{
		"empid": 1240,
		"empFirstName": "Mohammad",
		"empMiddleName": "salim",
		"empLastName": "ansari",
		"empsal": 150, 
		"empAddress": "Aurangabad",
		"empAge": 36
}


-------------CREAT TABLE
CREATE TABLE "EMP" 
   (	"EMPID" NUMBER(20,0), 
	"EMP_FIRST_NAME" VARCHAR2(50 BYTE), 
	"EMP_MIDDLE_NAME" VARCHAR2(50 BYTE), 
	"EMP_LAST_NAME" VARCHAR2(50 BYTE), 
	"EMPSAL" NUMBER(6,2), 
	"EMPADDRESS" VARCHAR2(100 BYTE), 
	"EMPAGE" NUMBER(3,0), 
	 PRIMARY KEY ("EMPID")
  );