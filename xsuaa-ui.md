# How to add the xsuaa authentication service to ui5 application.
1) create the xs-security.json file in your application and add the peace of code as shown below.
![image](https://user-images.githubusercontent.com/51018126/137128248-1e2db0b7-3266-418b-8d5c-38f9703b278a.png)
2) add the xsuaa configurations in MTA.yaml file.
    1) we need to add the serivce name under the module-->requires as shown below 
      ![image](https://user-images.githubusercontent.com/51018126/137128452-b894d30a-604f-4329-bca7-e061a48a5377.png)
    2) add the xsuaa service name, plan and path user the resources section as show below and the resouces should be in sequences based on requires section.
      ![image](https://user-images.githubusercontent.com/51018126/137128775-e92a5a87-394d-4d00-ae49-afa8c86d6469.png)
3) We need to add the authentication type under the your application/xs-app.json as shown below.
  ![image](https://user-images.githubusercontent.com/51018126/137128955-83bbbf61-a826-4aa9-b315-6494a2f7e9ed.png)
4) once everything added just build and deploy the application and try to open the application url it will ask for the authentication as shown below.
![image](https://user-images.githubusercontent.com/51018126/137129140-f2cb8915-ba5f-42e7-8496-5f8fca2d21e4.png)
