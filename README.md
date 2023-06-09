# PixelWaveOCR - Creating Digital Revolution

This codebase contains submission of Exact Sciences OCR Hackathon

### HomePage: [PixelWave OCR](https://ocr-hack-v0.web.app)
Visit: https://ocr-hack-v0.web.app
Video Link: https://www.youtube.com/watch?v=YPuUym2VCUM

To login, use the below default credentials:  
Username: admin  
Password: admin

### Processing: Requisition Form: 
  -  To upload and run OCR on a patient’s requisition form, choose the **Form 1** option after logging in. 
  -  In order to process a file, upload the file using **Choose files** option and then hit **Upload file** (Supported file formats are **.pdf, .jpg, .jpeg, .png, .tiff**). 
  -  Once the upload is successful, you’ll be automatically redirected to the processed form’s page (please wait about 5 seconds for this to happen). 
  -  If there are any corrections to be made, one can edit during this phase. After successfully making the required changes (incase of any discrepancy) hit on the **Submit** button and then confirm the same. 
  -  If you wish to export the response from our custom OCR API as a JSON, hit on **Export JSON** button. After successfully submitting the form, you will be redirected to the requisition form’s upload / search page.
  -  To search for a patient, use the **Patient ID or MRN** as the search value. While you are on the preview page, one can retrieve all the data on the form from the database.

### Processing: Information Needed Form: 
  -  The **Form 2** button has the provision to process and preview the 'Information Needed' page. The supported file formats remain the same. 
  -  On choosing the file and uploading it, you’ll be redirected to the page where you can make changes and then submit. 
  -  One can preview the submitted form using the 'Order number'. If no order number is mentioned then the default value will be randomly generated and stored. 

### Technology Stack:
 - **Backend** - Python
 - **Frontend** - HTML, CSS, Bootstrap, Javascript, JQuery
 - **Framework** - Flask
 - **Database** - Firebase
 - **OCR** - PixelWave Custom Model + Microsoft Computer Vision Read API
 - **API Hosting** - Azure App Services

### Executing it locally:
#### Pre-requisite:
1. Python 3.x and pip needs to be installed.  
2. Install Poppler (Ref: https://pypi.org/project/pdf2image/) 

#### Setup:
```sh
$ pip install -r requirement.txt
```
#### Data:
Maintain all the files to be tested in the same directory as app.py

#### Execution:
```sh
$ python app.py
```
#### To get json output use the following API endpoints:
Open the below links in a browser after replacing <file_name> with the filename of the file to be tested.
  - **Requisition form** - localhost:8000/reqtform/<file_name>/0
  - **Information Needed Form** - localhost:8000/reqtform/<file_name>/1  
Eg: To run OCR recognition in Information Needed form for filename as Sample.pdf, open browser with localhost:8000/reqtform/Sample.pdf/1
