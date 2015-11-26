# wso2-apim-hostobjects
Jaggery hostobjects for WSO2 store, used by developer portal API

This project adds the following functionality to the WSO2 store API:

1. Provides support for getting all API:s with status PROTOTYPED, PUBLISHED and BLOCKED in the same call, using pagination 

This is implemented as a new hostobject and modified jaggery files.

INSTALLATION

1. Build the Java jar file and place it in $CARBON_HOME/repository/lib
2. Copy the contents from store directory of this project to $CARBON_HOME/repository/deployment/server/jaggeryapps/store
3. Copy the contents of the modules directory of this project to $CARBON_HOME/modules

USAGE

To use this functionality, call:

http://localhost:9763/store/site/blocks/api/listing/ajax/list.jag with the following parameters

action=getPaginatedAPIs&tenant=carbon.super&start=0&end=-1

Note:

The list is 0-based, so to get rows from offset 1, use start=0. To retrieve all rows, use end = -1.

To install this 
