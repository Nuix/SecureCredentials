# SecureCredentials
This will allow for the encryption of Nuix credentials using DPAPI

If requested this script will allow for the encryption of user credentials to acquire a Nuix NMS or CLS license.

Prerequisties:
1. a Settings.json file to be located in the C:\ProgramData\Nuix\ProcessingFiles\ScriptAutomate folder
2. the Settings.json file to have an element named "dblocation": "C:\\Nuix\\DBLocation",

This application will show a simple dialog box requesting a username and password to be entered.  
Once the user presses the OK button the application will use the DPAPI (Data Protestion API) to encrypt the data and store the data in a file called nuixconfig.cfg in the 
dblocation referenced above

The secure credentials can be used in concert with any application that uses the Decrypt version of the DPAPI.  The settings.json file should have an element called
"useencryptedcreds":true, - if this element is present and the applications uses the DPAPI decrypt and references the nuixconfig.cfg file the credentials will be decrypted 
and can be used to access a Nuix license
