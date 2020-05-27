# PrepareBootcampUsers

Used internally at UiPath in order to mass-create System Admin users in a Process Mining instance. Each user is also given its own local git repository and environment. Currently, the username for a user is expected to be 

## Requirements
* Attended automation
* Built using UiPath Studio 2020.4.1
* Needs both Internet Explorer and Chrome to complete
* Optionally sends emails via local Outlook account

## Usage
* Click "Run"
* Enter server details (input screen)
** Enter the URL of the server hosting the Bootcamp, plus the credentials for the super admin user. 
** Optionally, you can enter a password that will be assigned to all newly-created users. Note that this must fulfill the Process Mining password requirements.
* Select Excel new-users Excel sheet
** Excel sheet is expected to have a header row, plus at least a column with the individual users' names and emails
* Specify creation details
** Specify the column (by name) in the Excel containing the users' common name and email address.
** Indicate whether the users should receive an auto-generated email
** (Optional) Enter the Subject and Body of the email, and whether it's HTML-based or not. The body replaces three placeholds: {url} the URL of the server; {username} the name the user needs to log into their account on the server; and {password}, the password for the account.
* Robot then creates the indicated users and adds a local git repo and an environment for each.
* Once complete, an Excel file containing the generated information (including password, git repo etc) is created an opened.
