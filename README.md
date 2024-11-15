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