# Network-Speed-Test-Continuous

i used chatGPT to help create a ping/network speed test that would log everything, i now have two versions of the script, the first will log the date and time it runs the test, the ping, the download and upload speeds, and the server that it ran the test on and records it into a .TXT file on your desktop, it will update the same txt file everytime it runs (i have it set to 15 minutes), it also tells you if you have a high ping, it will also log any errors and put that into a separate txt file


the second version (takes a bit more work to get working but is pretty simple to set up) is much more detailed
       
   this version will log the date and time it runs the test, the ping, the download and upload speeds, and the server that it ran the test on, it also records the average of the ping download and upload speeds, and it will log all of that information into a google spreadsheet, it will then use that information to create a graph and save it to your desktop as a .PNG to make it easy to visualize, it will also tell you (in the powershell/cmd prompt window), it will also tell you if youre below your expected speeds and by how much (percentage wise), it will also tell you if you have a high ping,
in order to run either of these scripts you will need to install python (as thats what the script was written in)
in order to do the second one though, i needed to 

Create a Google API Project:
Go to the Google Cloud Console.
Create a new project.
Enable Google Sheets API:
In your project, navigate to "Library".
Search for "Google Sheets API" and enable it.
Create Service Account Credentials:
Navigate to "APIs & Services" > "Credentials".
Click "Create Credentials" and select "Service Account".
After creating the service account, click "Manage Keys", then "Add Key" > "JSON". This will download a .json file containing your credentials.
Save the Credentials File:
Save this file as credentials.json in the same directory (desktop for me) as your Python script, or provide the correct path to it.
Share Your Google Sheet with the Service Account:
Open the Google Sheet where you want to store the results.
Click "Share" and add the service account email (found in the credentials file, typically ending with @<project-id>.iam.gserviceaccount.com) with "Editor" permissions.

im sure this could be converted into a batch file or service (or daemon for you linux users) somehow to allow it to run in the background but both versions will need the powershell/cmd prompt to be open (but can be minimized)
this was my first time writing a script and creating an actual github, feel free to edit the script for your situation or to add to or take away from it.
