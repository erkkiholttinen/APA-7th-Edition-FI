# APA 7th Edition (FI) for Microsoft Word

Until (unless) Microsoft gets around to adding a template for the latest version, this is the APA 7th Edition XSLT modified by Mike Slagle and Brian Kavanaugh. 

**IMPORTANT**: These files are provided as a courtesy to those needing a better option for APA 7 than what Microsoft currently provides when using Finnish language. I did not create the template, just modified it a bit. If there are issues, take the time to make the changes necessary (if possible; there are limitations to what can be done) and submit a pull request.

## How to Use

### Windows

#### Manual Method
1. Exit Word
2. Using Windows Explorer, copy the file APASeventhEditionFI.xsl to C:\Users\<your_user_name>\AppData\Roaming\Microsoft\Bibliography\Style 
3. Restart Word and from the References tab in Word, you should be able to choose APA7. 

#### Bat file method / Cmd method
1. Exit word
2. Copy the APASeventhEditionFI.bat file and allow it to run.
3. Restart Word and from the References tab in Word, you should be able to choose APA7. 

Note: The bat file simply runs the following line:
```
curl https://raw.githubusercontent.com/erkkiholttinen/APA-7th-Edition-FI/main/APASeventhEditionFI.xsl -o "%appdata%\Microsoft\Bibliography\Style\APASeventhEditionFI.xsl"
```



### MacOS

#### Manual method
1. Exit Word
2. Using Finder, copy the file APASeventhEdition.xsl to *two* locations:
    1. HD/Applications/Microsoft Word.app/Contents/Resources/Style/ (note that you will have to right-click and "View Contents" on the app icon at HD/Applications/Microsoft Word.app/)
    2. HD/Users/\<your_user_name>/Library/Containers/com.microsoft.Word/Data/Library/Application Support/Microsoft/Office/Style/
2. Restart Word and from the References tab in Word, you should be able to choose APA7. 

#### Shell script method / terminal method
* __The file asks for elevated priveliges using `sudo`. Only run files you trust and understand the contents of.__
1. Exit word and ensure it is closed before proceeding
2. Copy the APASeventhEditionFI.sh file to a local folder
3. Open the terminal (Search "Terminal through spotlight)
4. Navigate to the folder containing the shell script
    1. `cd /path/to/your/file`
5. Run the script
    1. `bash APASeventhEditionFI.sh`
    2. Enter password when prompted. The terminal stay blank while password is entered. Once entered, press enter
    3. The files should be placed in their corresponding folders

Notes:  
* The bash file will use the `curl` command to retrieve the file from github at the specified link and place it in the first of the specified folders above.
* It will then check if the file was placed in the folder successfully, and then copy the file from the first folder to the next.
* I do not have a Mac to test this on. The script was run successfully on a Mac with Office installed.


## Disclaimer

(same as Mike's and Brian's) I am only providing this file and the necessary location for it for education purposes. If any installations of MS Office are corrupted as a result of using this file, I am not responsible to address or repair any issues. 
