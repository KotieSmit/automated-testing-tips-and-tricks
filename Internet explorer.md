automated-testing-tips-and-tricks
=================================

Some tips and trick on automated testing that might come in handy

Internet Explorer
-----------------
- Long running scrips 
  http://support.microsoft.com/kb/175500
  - Using a Registry Editor such as Regedt32.exe, open this key:
  HKEY_CURRENT_USER\Software\Microsoft\Internet Explorer\Styles

  - Note If the Styles key is not present, create a new key that is called Styles.
  Create a new DWORD value called "MaxScriptStatements" under this key, and set the value to the desired number of script   statements. If you are not aure about which value you need to set this to, you can set it to a DWORD value of 0xFFFFFFFF   to avoid the dialog box.
  
- Self signed certificates
  http://stackoverflow.com/questions/681695/what-do-i-need-to-do-to-get-internet-explorer-8-to-accept-a-self-signed-certific
  How to make IE8 trust a self-signed certificate in 20 irritating steps

  - Browse to the site whose certificate you want to trust.
  - When told “There is a problem with this website's security certificate.”, choose “Continue to this website (not recommended).”
  - Select Tools➞Internet Options.
  - Select Security➞Trusted sites➞Sites.
  - Confirm the URL matches, and click “Add” then “Close”.
  - Close the “Internet Options” dialog box with either “OK” or “Cancel”.
  - Refresh the current page.
  - When told “There is a problem with this website's security certificate.”, choose “Continue to this website (not recommended).”
  - Click on “Certificate Error” at the right of the address bar and select “View certificates”.
  - Click on “Install Certificate...”, then in the wizard, click “Next”.
  - On the next page select “Place all certificates in the following store”.
  - Click “Browse”, select “Trusted Root Certification Authorities”, and click “OK”.
  - Back in the wizard, click “Next”, then “Finish”.
  - If you get a “Security Warning” message box, click “Yes”.
  - Dismiss the message box with “OK”.
  - Select Tools➞Internet Options.
  - Select Security➞Trusted sites➞Sites.
  - Select the URL you just added, click “Remove”, then “Close”.
  - Now shut down all running instances of IE, and start up IE again. The site’s certificate should now be trusted.
  
