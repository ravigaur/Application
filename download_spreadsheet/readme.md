
# Download spreadsheet using sheets api in python

This component is use for download spreadsheet using sheets api in python. This is an end to end process of downloading spreadsheet in any format,Steps are given below. 

	
1. Run Below command one by one -
	sudo apt-get update
    	sudo apt-get -y install python-pip
     	pip install --upgrade google-api-python-client
	
2. Now go to the below link - 
https://console.developers.google.com/apis/library/sheets.googleapis.com
    5.  If project already created select project else create new project
    6.  Click on ENABLE API
    7.  Now search for Google Sheets API, click on Google Sheets API.
    8.  Check Google Sheets API & Drive API are ENABLE or DISABLE if ENABLE then click on label.In below    screenshot API is already enabled
      
Then Go to credentials. (In top left)
    9.  At the top of the page, select the OAuth consent screen tab. Select an Email address, enter a Product name if not already set, and click the Save button.  

    10. Select the Credentials tab, click the Create credentials button and select OAuth client ID.
    11. Select the application type Other, enter the name , and click the Create button.
    12. Click OK to dismiss the resulting dialog. 
    13. Click the download icon (Download JSON) button to the right of the client ID.
	
    14.  Move this file to your working directory and rename it client_secret.json.
    15. Give access permission to the folder in which you want to download the file using below command
	cd path of folder 
sudo chmod 777 -R dirpath
    16.  Fill the credential in ini file , And run below command.
    17.  python fileDownloadfromGdrive.py 'fileDownloadfromGdrive.ini'

      18. Ini file parameter description are below.
    1. clientsecretkeypath = your dir path/client_secret.json
    2. spreadsheetid = your spreadsheet id
    3. filename = file name you want to save
    4. filepath = file path where you want to save
    5. mimetype = application/vnd.openxmlformats-officedocument.spreadsheetml.sheet
      19. Mime list is below:		
    1. MS Excel = application/vnd.openxmlformats-officedocument.spreadsheetml.sheet 
    2. Open Office sheet = application/x-vnd.oasis.opendocument.spreadsheet 
    3. PDF = application/pdf 
    4. CSV (first sheet only) = text/csv 
    5. TSV (first sheet only)  = text/tab-separated-values 
    6. HTML (zipped) = application/zip
