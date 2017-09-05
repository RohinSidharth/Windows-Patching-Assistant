# Windows-Patching-Assistant
Windows Patching Assistant tool based on PowerShell built for SCCM Environment.

Version 3.1 : Added Use of individual Credentials in input file


Version 3.0 : Needs to be run from the same domain as the target servers. No Credential support.


HOW TO USE

Input File: An input file can be generated from the tools menu>Export Template File. The FQDN column is mandatory.
The Domain user and Password column is optional. If you are running this app using an account that do not have admin permissions on target machines, you will run into access denied errors and will be shown in the monitoring screen. In that case populate this field with credentials of an account with admin permissions on the target machines. In case of Workgroup machines, the username should be in the format MachineName\username.

Begin button will start the monitoring. Will prompt for the input file if not already selected using the browse button.

Once the monitoring is started, the data will start getting populated. Give it about 3 minutes. The refresh time of the screen can be controlled by the up-down counter on the right side panel.

Double clicking a record on the monitoring screen will select it and activate the individual server control panel on the bottom. This gives you the ability to do micro management on that machine.

The “Enable Options” check box on the right side panel will grant you the ability to Push patches (if available to be pushed) and Reboot servers (if reboot is pending and no patches are installing/waiting) automatically on all the machines on the main monitoring screen. [Use with caution as this setting applies to all machines].

In case this is not running on your machine, you may have to set the PowerShell Execution policy correctly. Usually, setting it to ‘unrestricted’ would work.
