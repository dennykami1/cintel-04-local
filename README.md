# cintel-04-local
CONTINUOUS INTELLIGENCE Module 4: Professional Tools, Install Python

## Open a Terminal in VS Code
With a terminal open, click on the dropdown arrow next to the "+" icon in the terminal pane. It's the upper right of the terminal area. 
Select Select Default Profile.
Choose PowerShell from the list. This changes the default terminal type to PowerShell. From now on when you open a terminal, it will be PowerShell. PowerShell is the more modern terminal. These commands have been thoroughly tested to work in PowerShell.  

## Clone the GitHub Repository

cd ~\Documents

git clone url

## Access the Cloned Repository in VS Code
Use the File menu in VS Code to select "Open Folder", and choose the cloned repository folder

## Create Virtual Environment

py -m venv .venv

## Verify .gitignore includes .venv/

## Activate the Virtual Environment (often)

.venv\Scripts\Activate
.venv\Scripts\activate

## Install Dependencies  (as needed)

py -m pip install --upgrade pip setuptools

py -m pip install --upgrade -r requirements.txt

## Run the App

shiny run --reload --launch-browser penguins/app.py


## ShinyLive export to build the app in the penguins folder to the docs folder:

shiny static-assets remove
shinylive export penguins docs

## Run the following to serve the app:

py -m http.server --directory docs --bind localhost 8008

## Git Add / Commit / Push to GitHub

git add .

git commit -m "Your commit message"

git push -u origin main

## Change the Browser Tab Title
open the new docs folder. Edit docs/index.html - find the line that has the <title> and </title> opening and closing tags. The inner text between these two tags will appear in your tab.

<title>PyShiny Penguins</title>

## Add a Custom Favicon
Add your own custom favicon  (the little icon that appears in the web browser tab) next to the title. Try https://favicon.io/Links to an external site. and create a favicon

Download the zip file and extract the files. Take just the favicon.ico file and paste it into your docs folder.  Two changes are required:

Confirm there is a favicon.ico in your docs folder. 
Edit docs/index.html -  Just below the title line, add the following link tag like so. This code is the same for all of us - only the favicon appearance is different. If your favicon.ico has a different name or path, let VS Code help you provide the correct path. 

<title>PyShiny Penguins</title>
<link rel="icon" type="image/x-icon" href="./favicon.ico">

END