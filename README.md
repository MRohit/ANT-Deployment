# ANT-Deployment
ANT is a salesforce tool use to deploy components from one organization to another
Steps to deploy using ANT:

1. Create package.xml file and enter all the components which you want to retrieve. A sample package.xml can be found [here](https://github.com/MRohit/ANT-Deployment/blob/master/config/package.xml)
2. Edit [build.properties](https://github.com/MRohit/ANT-Deployment/blob/master/config/build.properties) and specify source and target username, password and URL.
3. Open command prompt where you've install ANT. You can specify source directory in build.xml where you want to retrieve files. Keep package.xml,build.properties and [build.xml](https://github.com/MRohit/ANT-Deployment/blob/master/config/build.xml) in same directory.
4. Enter command "ant retrieveOnly" will retrieve all the components specified in package.xml from respective source.
5. Enter command "ant validateOnly" will validate retrieved components on target org where we need to deploy.
6. Once package is succefully validated with no errors, enter command "ant deployOnly". This will deploy all the components on target org.
