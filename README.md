# Icon Request Dashboard
A simple to setup dashboard for Android icon pack makers. 

## How to set it up

1. Clone this repo
2. Open **docs/js/requests.js** Change the following line to your raw github requeests file txt: `https://raw.githubusercontent.com/Arcticons-Team/Icon-Request-Dashboard/main/generated/requests.txt`
3. Setup GitHub Pages in your repo's Settings: **Pages > Deploy from branch > main /docs**

## Process requests

1. Install Python if you haven't installed it
2. Install the dependencies
3. Run email_parser.py in a terminal: `email_parser.py mail_folder_path appfilter_path extracted_png_folder_path requests_path`
   (Change the paths according to your mail, appfilter, extracted png, and requests locations.) 
