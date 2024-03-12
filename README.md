# Icon Request Dashboard
A simple to setup dashboard for Android icon pack makers. <br>
It also checks your pull requests and removes the entries from the requests list.

## How to set it up

1. Clone this repo
2. Open `docs/js/requests.js` Change `Arcticons-Team` to your username and possibly `Icon-Request-Dashboard` to your project name too. : `https://raw.githubusercontent.com/Arcticons-Team/Icon-Request-Dashboard/main/generated/requests.txt`
3. Repeat the previous step for the combined appfilter. `https://raw.githubusercontent.com/Arcticons-Team/Arcticons/Icon-Request-Dashboard/docs/assets/combined_appfilter.xml`
4. Setup GitHub Pages in your repo's Settings: **Pages > Deploy from branch > main /docs**


## Process requests

1. Install Python if you haven't installed it
2. Install the dependencies
3. Download your e-mails and save them to `scripts/mails` for example (you can batch download mails easily with Thunderbird).
4. Run email_parser.py in a terminal: `email_parser.py mail_folder_path appfilter_path extracted_png_folder_path requests_path`
   (Change the paths according to your mail, appfilter, extracted png, and requests locations.)
This generates a `requests.txt` file and an `updatable.txt` if existing apps have updates. You can find the updatable file in the scripts folder when it's generated.

- **mail_folder_path** if you followed step 3 it should be `mail/`
- **appfilter_path** the folder where you keep your appfilter.
- **extracted_png_folder_path** the location to save all PNGs from icon requests `../docs/extracted_png`
- **requests_path** the path to your requests.txt file `../generated/requests.txt`
