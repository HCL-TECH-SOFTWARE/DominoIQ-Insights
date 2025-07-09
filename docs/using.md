# Setting up and Using DominoIQ Insights
![Screenshot DominoIQ Insights](assets/images/png/screenshot.png)

**This template is not intended for Web (browser) use and is not supported on the HCL Nomad platforms

This Domino application allows you to utilize the new DominoIQ AI engine in any custom Domino application.

## Installation of the Application:
### Deploy using template
This Domino application is provided as a Domino Template file. Follow the steps below to deploy it onto your Domino server:

1. Save the template into your Notes Data folder on your computer OR into the Domino Data folder on your Domino server
2.	Create a new Domino application with the Menu option “File-Application-New”
3.	In the dialog

 * Select the Domino server where you want to create this new application
 * In the “Title” field, enter “HCL DominoIQ Insights”
 * In the “File name” field, enter “domiq_insights.nsf”
 * For the Template Server, select “Local” if the template is on your computer or select the Domino server where you placed the template
 * In the list of Templates, select “HCL DominoIQ Insights” 
 * Press the “OK” button to create the application
<br/><br/>

## Configuring HCL DominoIQ Insights
Once the new application has been created, there are two additional steps to perform:

### Setup Access Control List (ACL)
Upon initial creation, some ACL entries are automatically set:

-	“Default” and “Anonymous” are set to “No Access”
-	“LocalDomainAdmins” and “LocalDomainServer” are set to “Manager” with the “[Admin]” role 
You will need to adjust the ACL to allow others to be ‘End users” and “Configurators” of the application as follows:
-	“Configurators” will need a minimum of “Editor” ACL access and the “[Admin]” role
-	“End Users” will require “Author” ACL access

### System Settings
One the application is opened for the first time the Administrator or Configurator needs to click on the “System Settings” entry on the Navigator. This will open the “System Settings”. Once opened, the user needs to select their primary “DominoIQ” server. Once selected, the user must click the “Save & Close” Actionbar button.
<br/><br/>

## Configuring a Custom Domino Application
To use DominoIQ Insights in your custom Domino applications, you must first configure them within this application.

To perform this configuration, follow the steps below:

1.	Click “App Configurations” on the Navigator
2.	In the View, click the ‘New App Configuration” Actionbar button
3.	Click the icon next to the label “Domino Application” and select the custom Domino Application you want to configure
4.	Select the Form that you want to enable for DominoIQ Insights usage
5.	Select the Fields that you want to allow DominoIQ to work with and then press the ‘Add” button
6.	If desired, for each Field selected you can provide a more readable Field Label. Select the Field, then enter the Field Label, and then press the “Update” button. Repeat for each Field that you want to have a Field Label for.
o	The Field Name is used by default. Field Labels are also provided to DominoIQ which will provide a better result. 
7.	Select the “DominoIQ Command(s)” that you want to allow users to use from the list provided
8.	Once satisfied with the values selected, press the “Push Settings to Application” Actionbar button
<br/><br/>

## Using DominoIQ Insight in the Custom Domino Application
When a DominoIQ Insights enabled custom Domino application is opened, the End Users will now be able to use DominoIQ on the enabled data.

The process is very simple:

1.	Open a Document or select multiple Documents within a View (maximum 10 documents at this time can be selected)
2.	From the “Actions” Menu, select “DominoIQ Insights”
3.	In the DominoIQ Insights Wizard, provide additional prompt information (optional)
4.	Select the DominoIQ Command to use if multiples were configured – if only one Command was configured, this step can be skipped
5.	Press the “Get Results” button. The result will be displayed 
6.	Two additional features will also be displayed: 
 * “Email Result”: This will generate a Notes Email with details from the DominoIQ Insights Request (Initiator, Domino Application where used, and the result)
 * “Copy Result”: this will copy the DominoIQ result onto the user’s clipboard

DominoIQ Insights can also store the results for review at a later time. The End User can open the DominoIQ Insights application from their Notes Workspace. They will see a View of all their previous results. 

The End User will have the ability to “Refresh Insights” (perform the same DominoIQ Request as previously and stored new result). 

This can be done both from an open DominoIQ Insights Results document or by selecting the document in the View and pressing the “Refresh Insights” Actionbar button.

The End User can also share the DominoIQ Insights Results with others that they feel would benefit. This is also performed in the View by pressing the “Share” Actionbar button. When the “Share” dialog is presented, they will have the ability to add other End Users, send an email to those new End Users, and/or copy a link to the DominoIQ Insights Results document onto their clipboard.

When the other End users open the DominoIQ Insights application, they will see these Results documents in the “Shared DominoIQ Insights” View.
