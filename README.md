# Web Engineering 2016-2017 / Microservices

1. The two microservices are running and registered (two terminals, logs screenshots).

   Accounts Microservice
   
   ![Accounts_Microservice_Terminal] (screenshots/2222.png)
   ![Accounts_Microservice_Web] (screenshots/2222W.png)

   Web Microservice
   
   ![Web_Microservice_Terminal] (screenshots/33333.png)
   ![Web_Microservice_Web] (screenshots/3333W.png)

2. The service registration service has the two microservices registered

   ![Registration_Service_Terminal] (screenshots/1111.png)
   ![Registration_Service_Web] (screenshots/1111W.png)

3. A second account microservice is running in the port 4444 and it is registered

   Accounts Service number 2

   ![Accounts_Microservice_4444_Terminal] (screenshots/4444.png)
   ![Accounts_Microservice_4444_Web] (screenshots/4444W.png)
   
   Registration service with both accounts
   
   ![Accounts_Microservice_4444_Web] (screenshots/11112W.png)
   

4. A brief report describing what happens when you kill the microservice with port 2222.
Can the web service provide information about the accounts? Why?

When someone kills the account server running at port 2222, the registration service on port 
1111 is notified by the web microservice. After a short time, the registration microservice 
notices that there is another account microservice endpoint, running on port 4444 so it 
continues to provide access to the account microservice from that port. 