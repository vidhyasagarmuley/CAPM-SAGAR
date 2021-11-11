# List of commands and their functionalities.
 yo --> this command used to create the new applications.
cf e ibsoqualitydash-approuter --> this command will show the nevironment variables configuration(lis of configuration services).
cf e ibsoqualitydash-approuter --export-json default-env.json ---> to export the environments variable in to json file.
cf a -- > this will show list of apps deployed into BTP.
cf marketplace --->  to get the service plans 
cf undeploy cpapp --delete-service-keys --delete-services --> to undeploy the cap application
# cf env ibsoqualitydash-srv  > default-env.json -- > When testing the service locally and you get an error saying No service matches destination then you need to look into getting the destination credentials from SCP.
