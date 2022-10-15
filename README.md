# JasonpowerDB
## Introduction to JsonPowerDB

## Steps for creating Developer Account
visit the JsonPowerDB login page

JsonPowerDB Login Page (login2explore.com)

Register yourself by clicking on the Register button

after registering, you'll get your credentials in your email

That's it, your Developer Account has been created

## Steps to Generate Token
Simply go to the above mentioned website and Login

After which you'll see a dashboard like this
![Dashboard](/Images/dashboard.png)

Click on the Tools tab

Under Token tab you'll find Generate Connection Token button. So, simply click on it.

Now you are all set to use JsonPowerDB.

## Some Features of JsonPowerDB
- Serverless Support - fast development - cuts time to market
- Schema free - easy to maintain
- Multi-Mode database - one solution to variety of data
- Build around worlds fastest* indexing engine PowerIndex
- Nimble, Simple to use, In Memory, Real-Time
-  Webservices API - low development cost
- A single instance - Million Indexes
- Inbuilt support to Querying Multiple Databases
- Server Side Native NoSQL - best performance
- Multiple security layers

## Why Prefer JsonPowerDB ?
- Minimum Development Cost
- Minimum Time to Market
- Minimize the complexity of interoperability of different applications
- Maximum data processing performance
- Technology Futuristic
	- Fills gap from database to big-data
	- Pluggable with new algorithms
	- Pluggable and user defined API
- Minimize Total Cost of Ownership

## Basic commands
## Insert Single Record

- Syntax
	```
	{
		"token": <"connection-token">,
		"cmd": "PUT",
		<<"dbName": <"database-name">,>>
		<<"rel": <"relation-name">,>>
		<<"colsAutoIndex": <boolean-value>,>>
		<<"templateStr": <jsonTemplateStr>,>>
		"jsonStr": <jsonDataStr>
	}
	
- Some important points to keep in mind
	- Http Method : POST
	- Base URL : http://api.login2explore.com:5577
	- End-point URL : /api/iml 
-  Code Sample
	```
	{
    		"token": "90937699|-31949297143690297|90942402",
   		 "cmd": "PUT",
   		 "dbName": "Student",
    		"rel": "Student-Rel",
   		 "jsonStr": {
        		"id": "1",
			"name": "rugved",
       		 "email": "rugved02@gmail.com",
       
    		}
	}
	```
![PUT](/Images/put1.png)
![PUT](/Images/put2.png)
![PUT](/Images/put4.png)

## Retrieve Single Record
- Some important points to keep in mind
	- Http Method : POST
	- Base URL : http://api.login2explore.com:5577
	- End-point URL : /api/irl 
- Syntax
	```
	{
		"token": <"connection-token">,
		"cmd": "GET",
		"dbName": <"database-name">,
		"rel": <"relation-name">,
		"jsonStr": {
			<"ColumnName":"JsonValue">
    	}
	}
	```
- ![GET](/Images/get1.png)


## Update Multiple Record
- Some important points to keep in mind
	- Http Method : POST
	- Base URL : http://api.login2explore.com:5577
	- End-point URL : /api/iml 
- Syntax
	```
	
### Update Single Record
- Some important points to keep in mind
	- Http Method : POST
	- Base URL : http://api.login2explore.com:5577
	- End-point URL : /api/iml 
- Syntax
	```
		{
    	"token": <"connection-token">,
   	 "cmd": "UPDATE",
    	<<"dbName": "database-name",>>
    	<<"rel": "relation-name",>>
    	"jsonStr": {
       		 <"record-no">: {
            		<"column-name">: <"new-value">
        		}
        	<"record-no">: {
            		<"column-name">: <"new-value">
        		}
   	 	}
	}
	```
- code sample 
 	```
	{
    		"token": "90937699|-31949297143690297|90942402",
   		 "cmd": "UPDATE",
      			"dbName": "Employee",
     			 "rel": "index",
   		 "jsonStr": {
         		"3" : {
            			 "name" :  "akhil 81"
        			}
         		"2" : {
            			 "password" :  "abcd"
        			}
    			}
		}
	```
- ![UPDATE](/Images/update1.png)
- ![UPDATE](/Images/update2.png)
- ![UPDATE](/Images/update3.png)
- ![UPDATE](/Images/update4.png)

## Remove Single Record
- Syntax
	```
	{
		"token": <"connection-token">,
		"cmd": "REMOVE",
		"dbName": <"database-name">,
		"rel": <"relation-name">,
		"record": <record_number | [recNo1, recNo2....]>
	}
	```
- Code Sample
	```
	{
    		"token": "90937699|-31949297143690297|90942402",
    		"cmd": "REMOVE",
      		"dbName": "Employee",
      		"rel":  "index",
   		"record": 2,
    		"jsonStr" : {}
	}
	```
- ![REMOVE](/Images/remove1.png)
- ![REMOVE](/Images/remove2.png)
- ![REMOVE](/Images/remove3.png)
