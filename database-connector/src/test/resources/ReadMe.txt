--select-operation
	POST /select HTTP/1.1
	Host: localhost:8081
	Content-Type: application/json
	Cache-Control: no-cache
	Postman-Token: a5c534df-2034-22e5-af29-40586449a72e
	
	{
		"empid":1235
		
	}
	
	
--update-operation
	POST /update HTTP/1.1
	Host: localhost:8081
	Content-Type: application/json
	Cache-Control: no-cache
	Postman-Token: af66e26d-7e37-be50-f7c6-f5ee9af16012
	
	{
		"empid": 1234,
		"increment": 5
	}
	
--insert-operation
	POST /insert HTTP/1.1
	Host: localhost:8081
	Content-Type: application/json
	Cache-Control: no-cache
	Postman-Token: f85e9b08-7492-3cd3-787b-a9e5f8e30ee5
	
	{
		"empid": 1238,
		"empFirstName": "Mohammad",
		"empMiddleName": "salim",
		"empLastName": "ansari",
		"empsal": 150, 
		"empAddress": "Aurangabad",
		"empAge": 36
	}
--delete-operation
	DELETE /delete HTTP/1.1
	Host: localhost:8081
	Content-Type: application/json
	Cache-Control: no-cache
	Postman-Token: 497da2f7-54f8-4a0b-a2a8-4b42df85294c
	
	{
		"empid":1239
	}
	
--bulk-preration--
	POST /bulk HTTP/1.1
	Host: localhost:8081
	Content-Type: application/json
	Cache-Control: no-cache
	Postman-Token: 7dadf3d4-832e-3e73-48b1-0be2fc7a26fa
	
	{
		"empid":1238,
		"newid":1239
	}
--store-procedure-operation
	PUT /procedure HTTP/1.1
	Host: localhost:8081
	Content-Type: application/json
	Cache-Control: no-cache
	Postman-Token: c9033cd2-0e92-99a1-ca24-1940b5702065
	
	{
		"empid": 1233,
		"increment": 1.5
	}
	--CREAT TABLE
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
 --PROCEDURE
 create or replace PROCEDURE salary_increment(
    in_employee_id IN NUMBER,
    in_percent IN NUMBER, new_sal OUT NUMBER
) IS
BEGIN
   UPDATE emp SET empsal = empsal + empsal * in_percent / 100
   WHERE empid = in_employee_id;
   SELECT EMPSAL INTO new_sal FROM EMP WHERE EMPID = in_employee_id;
END;
	