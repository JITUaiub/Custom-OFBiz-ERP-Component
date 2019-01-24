# Custom-OFBiz-ERP-Component
Custom Module usign Apache Ofbiz

Development with Apache OFBiz Framework
How to get started with Apache OFBiz

Author: Md. Nashid Kamal Jitu

Download Apache OFBiz Framework
Download from here: http://svn.apache.org/repos/asf/ofbiz/branches/release16.11
Running Apache OFBiz
Start for Windows: > gradlew loadDefault ofbiz
Turn off for Windows: > gradlew "ofbiz --shutdown"
Create the plugin/component
For Windows: > gradlew createPlugin -PpluginId=ofbizDemo -> It will be created under specialpurpose folder. It can be run using: https://localhost:8443/ofbizDemo. Here, ofbizDemo is new component name.
 
CHAPTER 1: ENTITY
1.1 Creating First Database Entity (Table) 
Entity definition should be placed under $OFBIZ_HOME/specialpurpose/ofbizDemo/entitydef/
entitymodel.xml file. Also need a root declaration under $OFBIZ_HOME/specialpurpose/ofbizDemo/
ofbiz-component.xml file. Let’s see the definition structure.

entitymodel.xml:
ofbiz-component.xml:
1.2 Insert data to Entity(Seed/Demo data): 
Method 1: We can place our raw data to $OFBIZ_HOME/specialpurpose/ofbizDemo/data/OfbizDemoTypeData.xml file. We’ll place only final data to this file, like the data which must need to operate a application. Example:
OfbizDemoTypeData.xml
We can place our demo data to $OFBIZ_HOME/specialpurpose/ofbizDemo/data/OfbizDemoDemoData.xml file. We’ll place only demo data to this file, like the data which must need to test on this application. So we can remove demo data ealisy from <entity-resource> definition. Example:
OfbizDemoDemoData.xml
Method 2: We can load data using Entity Manager as well. For so, go to https://localhost:8443/webtools/control/EntityImport. Simply put your xml data in " Complete XML document (root tag: entity-engine-xml):" text area and hit "Import Text". Here is an Example: 
1.3 Testing Entity Objects: 
To check entity, go to https://localhost:8443/webtools/control/entitymaint, then login using username “admin” and password “ofbiz”. You’ll be able to see all entity objects. Find the entities that you already defined. You can see the data you’ve inserted as well.
1.4 Appendix: 
To find more deep information about Entity Engine (includes overview, all attribute documentation), Please refer to this link: 
https://cwiki.apache.org/confluence/display/OFBIZ/Entity+Engine+Guide 
CHAPTER 2: SERVICE
Services are small piece of logic that process different types of business logic. 
1.1	Testing Entity Objects: 
To
1.4 Appendix: 
To find more deep information about Entity Engine (includes overview, all attribute documentation), Please refer to this link: 
https://cwiki.apache.org/confluence/display/OFBIZ/Service+Engine+Guide 
CHAPTER 3: USER INTERFACE
1.1 Creating a Simple UI:
