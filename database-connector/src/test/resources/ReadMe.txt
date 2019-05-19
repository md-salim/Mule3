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
			