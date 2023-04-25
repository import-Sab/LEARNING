found below note, please try if useful.



3247817 - #SCC handshake failed: 500 — Internal Server Error when adding subaccount to Cloud Connector

Version 3 from 28.09.2022 in English

Symptom

When trying to add a new Subaccount to the SAP Cloud Connector, you receive the following message:

417 Could not download configuration file. See "Log And Trace Files" and in particular ljs_trace.log for details. Consult SAP note 2460641 for possible remedies.

When checking the ljs_trace.log file for more information, it's possible to see the following logs:

<date and time> #INFO#com.sap.scc.security#https-jsse-nio2-8443-exec-8# #Returned Http Response with code 500
<date and time> #INFO#com.sap.scc.config#https-jsse-nio2-8443-exec-8# #Stopping service channels on <Subaccount>
<date and time>#ERROR#com.sap.scc#https-jsse-nio2-8443-exec-8# #SCC handshake failed: 500 — Internal Server Error
com.sap.scc.servlets.SccHandshakeException: SCC handshake failed: 500 — Internal Server Error









Environment

SAP Business Technology Platform;

SAP Cloud Connector.

Reproducing the Issue

Log on to the SAP Cloud Connector.


Click the Add Subaccount button.

Cause

The Cloud Connector version is outdated;

The password being utilized in the configuration is wrong.

Resolution

Check if the SCC version being used is the latest one, as per 2539713 - Upgrade to a new version of the Cloud Connector.


In case the Cloud Connector is up-to-date, check if the password you're utilizing is correctly associated with the e-mail account and Subaccount utilized in the configuration. The user must also be an administrator of the subaccount.
To check the password, you can try to login against https://accounts.sap.com/ using the same user and password.
