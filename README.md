iHRIS + JasperSoft Server Connector
===================================

Communication
-------------
Use #idhack2016 Slack channel for iHRIS team: https://ihris.slack.com/archives/idhack2016

Project Overview
----------------
iHRIS is a suite of open­source software designed for health ministries of health to manage their health workforce. It has been deployed in approximately 25 countries and contains information on over one million health workers (See http://www.ihris.org/about/ihris­countries/​).

Although iHRIS has a built­in reporting system that can meet basic analytical needs, more powerful and easier to use tools are needed. This project would link iHRIS to the open­source Jasper SoftStudio report designer in order to provide additional analytical tools off the iHRIS back­end data store (MySQL).
Jasper Soft Studio (See h​ttp://community.jaspersoft.com/project/jaspersoft­studio)​is the free, open source, eclipse­based report designer for JasperReports and JasperReports Server.​Jasper Soft Studio can be used to create very sophisticated layouts containing charts, images, subreports, crosstabs and much more.

iHRIS has a flexible and dynamic data model which is exposed with an API. The project will query the iHRIS data model to pre­populate data sources for Jasper Reports from a particular iHRIS installation so that the data sources are automagically available to the end user of Jasper SoftStudio. This project will use an instance of iHRIS with can be installed using Ubuntu 14.04 (LTS) using apt­get and which contains a demonstration data set (See h​ttp://wiki.ihris.org/wiki/Installing_iHRIS_4.2​)

The project should produce documentation on the iHRIS wiki needed steps to replicate the integration and example YouTube videos demonstrating the report generation functionality.

All artifacts produced under the project should be released under an appropriate open
source or Creative Commons license.


iHRIS Resources
---------------
- Install iHRIS (ihris-manage-site-demo) http://wiki.ihris.org/wiki/Installing_iHRIS_4.2
- (outdated) eLearning course on iHRIS http://www.hrhresourcecenter.org/elearning/course/view.php?id=4
- iHRIS Manage Forms and Fields in Demo site http://wiki.ihris.org/wiki/IHRIS_Manage_Form_Fields_-_4.1.4
- iHRIS Qualify Forms and Fields http://wiki.ihris.org/wiki/IHRIS_Manage_Form_Fields_-_4.1.4
- Liberia Forms and Fields http://wiki.ihris.org/wiki/Liberi_iHRIS_Manage_Data_Elements
- iHRIS Magic Data XML format http://wiki.ihris.org/wiki/Configuration_%28Magic%29_Data
- Magic Data for Form Classes http://wiki.ihris.org/wiki/Form_Fields
- Magic Data for Forms http://wiki.ihris.org/wiki/Defining_Forms
- Caching Forms wiki.ihris.org/wiki/Form_Caches
- iHRIS Custom Reports http://wiki.ihris.org/wiki/Custom_Reporting
- iHRIS source code and customizations https://launchpad.net/ihris-suite



iHRIS API Endpoints
-------------------
Once installed according to above, you can access iHRIS at http://localhost/ihris-manage-demo  Username = i2ce_admin password is mysql password on install.

You can execute a GET request with HTTP BASIC AUTH for Magic Data Export at 
   http://localhost/ihris-manage-site-demo/magicDataExport/export 
The query parameters are:
- config_path: (required) the Path in magic data you want to export data from.  See links above.
- name:  (required) You are exporting data into an iHRIS module.  This just a name to identify the module.  Probably not useful but should be set.
- displayName: (optional) Human readable name describing the 
- description: (optional) description of the data you are exporting
- version: (optional) version of the data you are export.  
This will return an XML file $name.xml where $name is the name set above.


  


Jasper Resources
----------------
- Web Services Introdution http://community.jaspersoft.com/documentation/tibco-jasperreports-server-web-services-guide/v62/introduction
- JRXML: Jasper Reports XML definition language http://www.tutorialspoint.com/jasper_reports/jasper_report_designs.htm
- More JRXML: http://community.jaspersoft.com/documentation/tibco-jaspersoft-studio-user-guide/v60/jrxml-sources-and-jasper-files
- RESTful Web Serverices Overview http://community.jaspersoft.com/documentation/jasperreports-server-web-services-guide/v56/rest-web-services-overview
- Adding a Custom Data Source: http://community.jaspersoft.com/wiki/adding-custom-datasource-using-jasperreports-server-webservices-apis
- Web Services API overview  http://community.jaspersoft.com/wiki/getting-started-rest-web-service-api
- Creating Reports programatically http://community.jaspersoft.com/wiki/how-programmatically-create-reports-jasperreport-server
