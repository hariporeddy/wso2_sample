# Summary
This document gives the details of my sample project of wso2.

## I have used wire mock to run my mock rest api.
##  Please follow below steps to up and run mock rest api.


1. Unzip Hari_MockRestApi.zip file
2. Then navigate to folder where you have unzipped above zip file and run below command.
```
java -jar wiremock-standalone-2.21.0.jar --port 8585

```
 3. This Mock Rest APi providing two apis as below
 
 ```
 http://localhost:8585/deptcontext/departments/dept1 which give department 1 details
 
 http://localhost:8585/empcontext/employees/emp1 which give employee 1 details
 
 ```
 
 4. I have exposed both above apis to ESB as EmpEndpoint and DeptEndpoint.
 
 5) WSo2 OrganisationApi meadiate to above two apis dependent on uri condition. Below first one 
 forward to http://localhost:8585/deptcontext/departments/dept1  and 
 second one forward request to http://localhost:8585/empcontext/employees/emp1.
 
   ```
   http://localhost:8280/organisation/queryName/dept1
   http://localhost:8280/organisation/queryName/emp1
    ```
	
## I have attached car file and source code of car as HariHmrcComposite.zip. 
 
 
 
 