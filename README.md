# Icon Request Dashboard
A simple to setup dashboard for Android icon pack makers. <br>
It also checks your pull requests and removes the entries from the requests list.

## See it in Action
[Arcticons](https://arcticons-team.github.io/Arcticons/requests.html)<br>
[Dollphone-Foss](https://2gd4.me/dollphone-foss/requests.html)

## How to set it up

1. Clone this repo
2. Setup GitHub Pages in your repo's Settings: **Pages > Deploy from branch > main /docs**
(Using it with localhost is possible too, if you don't use the GitHub actions) 

### the Github actions

If you want to use the GitHub action to filter out entries that are present in a pull request, you need to 
open `.github/workflows/combine_appfilter.py` Change the Repository an the Branch to yours.
this requeres the repo to be the same as the one that gets the pull requests.

## Process requests

1. Install Python if you haven't installed it
2. Install the dependencies
3. Download your e-mails and save them to `scripts/mails` for example. (You can batch download mails easily with [Thunderbird](https://www.thunderbird.net/en-US/).)
4. Run email_parser.py in a terminal: `email_parser.py mail_folder_path appfilter_path extracted_png_folder_path requests_path`
   (Change the paths according to your mail, appfilter, extracted png, and requests locations.)
This generates a `requests.txt` file and an `updatable.txt` if existing apps have updates. You can find the updatable file in the scripts folder when it's generated.

- **mail_folder_path** if you followed step 3 it should be `mail/`
- **appfilter_path** the folder where you keep your appfilter.
- **extracted_png_folder_path** the location to save all PNGs from icon requests `../docs/extracted_png`
- **requests_path** the path to the folder containing your requests.txt file `../docs/assets/`
