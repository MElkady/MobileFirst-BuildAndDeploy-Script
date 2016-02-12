## Note
Before running this script make, sure to:
- Place "worklight-ant-builder.jar" & "worklight-ant-deployer.jar" files in the same directory as build.xml.
- Modify build.properties with your configuration

## Ant targets:
- buildWar: to build the WAR file
- buildApps: to build WLAPP files
- buildAdapters: to build adapter files
- buildAndroid: to build APK file. Make sure to call buildApps target at least once before running buildAndroid
- packClients: to package clients as ZIP files if you want to build it later.  Make sure to call buildApps target at least once before running packClients
- buildServer: One target to call buildApps, buildWar, buildAdapters & packClients
- deployAdapters: to deploy adapters to MobileFirst server
- deployApps: to deploy WLAPP(s) to MobileFirst server
- deployAll: one target to call deployAdapters & deployApps
- buildDeployServer: one target to call buildServer & deployAll
- buildDeployAdapters:  one target to call buildAdapters & deployAdapters
- buildDeployApps:  one target to call buildApps & deployApps

The build script will place output files in the directory specified by the property "build.dir" in "build.properties"