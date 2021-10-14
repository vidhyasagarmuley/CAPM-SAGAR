# How to fetch the logged in user details in SAP UI5 CAP project using jwt token.
1) To fetch the logged in userd details first we need to add the xsuaa configurations and approuter to the application these steps are already available in the following files in the same repo the file names are xsuaa-ui.md, README.md  under the same repo.
2) Next step is we need to create the JS file like approuter-start.js under application-->approuter folder and add the peace of code in the file as follows.
  ![image](https://user-images.githubusercontent.com/51018126/137258672-ef19a406-2e1f-40e3-bc80-56a3d1f1fab8.png)
3) Then add the jwt dependencies and script code in the package.json file under the app router as shown below once we update the package.json file run npm install to install the dependencies.
  ![image](https://user-images.githubusercontent.com/51018126/137258964-4ef6c3ac-334c-43cc-be72-b2646f4ccd36.png)

4) After performing above steps we need to call the api in our code as follows, in my case i will call the api in componenent.js file.
  ![image](https://user-images.githubusercontent.com/51018126/137260068-c476f905-75a5-4099-9f73-0862e195dfe0.png)
5) build the project and deploy it, you will see the details of the logged in user as shown below.
   ![image](https://user-images.githubusercontent.com/51018126/137261305-7d41c40b-63c4-40b7-a091-a91ed912107a.png)
   ![image](https://user-images.githubusercontent.com/51018126/137261587-c935df04-2a9f-4b1d-bed2-3a2112007b6c.png)


