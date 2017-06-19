#################
Configuration
#################

***************************************
Azure App Service Application Settings
***************************************

* Java Version: Java 8
* Java Minor version: Newest
* Web container: Newest Jetty 9.3
* App Settings:
    - Environment variable 'DEP_ENV' set to 'devtest', 'staging' or 'prod' as appropriate.
    - Deployment slot names: 'dvasopapi-dev, dvasopapi-devtest', 'dvasopapi-staging', 'dvasopapi' (production).
* web.config file in the repository root enforces redirection to https:// endpoint.
* CORS enabled via Azure management interface.
* DEP_ENV environment setting set via Azure management interface as follows: 

+-------------+---------+------------------+------------+-------------------------+
| Environment | DEP_ENV | Deployment Slot  | Git Branch | Azure Storage Account   |
+-------------+---------+------------------+------------+-------------------------+
| dev         | devtest | dvasopapi-dev    | devtest    | dvasopapistoragedevtest |
+-------------+---------+------------------+------------+-------------------------+
| devtest     | devtest | dvasopapi-devtest| devtest    | dvasopapistoragedevtest |
+-------------+---------+------------------+------------+-------------------------+
| staging     | prod    | dvasopapi-staging| master     | dvasopapistorage        |
+-------------+---------+------------------+------------+-------------------------+
| production  | prod    | dvasopapi        | master     | dvasopapistorage        |
+-------------+---------+------------------+------------+-------------------------+

* See AppSettings.java for other expected environment variables.
* If the JVM property ```DEV_ENV``` is set to 'devtestlocal', this indicates the app is running on a local development machine.  This means the local Azure store emulator is used.
* No handler mappings in Azure management interface
* Virtual Applications and Directories: '/','site\wwwroot', Application.
