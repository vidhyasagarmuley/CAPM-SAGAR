#  How to create the destinations in BTP and consume the odata services from another MTA CAP project into ui5 application
1) We need to create the destination in BTP account as follows connectivity->detinations-->create new destination.
2) please refer below snap.
![image](https://user-images.githubusercontent.com/51018126/137075112-aa3fe26e-449d-48c3-bea5-92454c5d7ae5.png)
if its an uua service then we need to configure the destinations as follows 
![image](https://user-images.githubusercontent.com/51018126/137075534-f6785cc3-8820-448b-8a25-8709d8ff8ba2.png)
in the above snap 
    1) url: url is nothing but cap odata service url or cap node.js project url
    2) Authentication: OAuth2UserTokenExchange
    3) Client ID, Client Secret and Token Service URL: client ID nothing but uua service client ID goto spec->applications
    ![image](https://user-images.githubusercontent.com/51018126/137075949-48775de6-dc9b-418a-8ba9-bc8a713ab0f3.png)
    4) then click on the application link
    ![image](https://user-images.githubusercontent.com/51018126/137076127-9d9595f8-97f7-4af6-8b1e-7216b2e54b14.png)
    5) got to Environment Variables and then you will get the required info as follows
    ![image](https://user-images.githubusercontent.com/51018126/137076645-0c86db1e-5737-4242-8d80-18e3b769436d.png)
      Note token url is nothing but url + outh/token = https://e8a6dd9ftrial.authentication.eu10.hana.ondemand.com/oauth/token
    Now we have configured the dentination at cloud account then next step is we need to consume it in our application if we have seperate UI and Backend CAP project then we       need to consume it in both the apps.
3) Goto your ui application in BAS add the code as follows.
    1) open MTA.yaml file under the modules->requires
    ![image](https://user-images.githubusercontent.com/51018126/137077381-c528b349-8cbe-4deb-9a8e-e20736d5fb00.png)
      after adding the destination name over there then we need to add the destinations services in resources section as show in the below snap.
      ![image](https://user-images.githubusercontent.com/51018126/137077701-6a13d9cd-fc78-449f-8941-7d4021e6d9e8.png)
    2) goto xs-app.json file and add the destination as follows.
     ![image](https://user-images.githubusercontent.com/51018126/137077883-cba937e6-70b5-48ec-a3ec-fab374f707ed.png)
     Now we have consumed the destiantion services in our UI application next step is we need to add the same in backend CAP project if we have separate backend project.
 4) Goto your backend CAP project in BAS add the code as follows.
     1) open MTA.yaml file under the service module->requires
        ![image](https://user-images.githubusercontent.com/51018126/137078363-27cc5311-3383-40cb-bc37-176de42ddb4e.png)
        after adding the destination name over there then we need to add the destinations services in resources section as show in the below snap.
        ![image](https://user-images.githubusercontent.com/51018126/137078615-d9499559-4e9a-43af-8dbd-016185f62c4e.png)
5) Now you have configured the destinations in BTP cloud and consumed the services as well just for the info how we need to add the service in manifest.json file in UI application as follows.
    ![image](https://user-images.githubusercontent.com/51018126/137079018-88f836ca-1e2b-4c23-9c1f-37261ec5c764.png)
    the uri path we need to mentio as like /browse/ in my case which is shows in above snap same like how we add the service uri for the onprimie system (sap/opu/data).
    


    

