# TouchSelfie
Open Source Photobooth based on the official Raspberry Pi 7" Touchscreen

Starting with a new install of Raspian on your Raspberry Pi 3B or 3B+, run the following commands individually:
```
sudo apt-get update
sudo apt-get install python-imaging
sudo apt-get install python-gdata
sudo apt-get install python-imaging-tk

sudo pip install --upgrade pip
sudo pip install --upgrade google-api-python-client
sudo pip install --upgrade oauth2client

mkdir git
cd git
git clone https://github.com/wyolum/TouchSelfie
or
git clone https://github.com/carolinedunn/TouchSelfie

```
Still on your Raspbian desktop, open Chromium, the pre-loaded, default web browser.
Sign into your Gmail account.
Go to Account Security Settings: https://myaccount.google.com/security
Ensure 2-factor authentication is turned on.
Create a Photo Album. Note: Photo Albums require at least 1 photo.
Create an App Password

Open a new tab in your browser and goto: https://console.developers.google.com/
Create a new project.
Click Enable APIs
Enable Gmail and Drive APIs.
Create OAuth2 credentials
Download OAuth2 credentials

On your Raspian desktop, open your file manager.
Rename the .json file you just downloaded to OpenSelfie.json
Move OpenSelfie.json to /home/pi/git/TouchSelfie/scripts

In your Raspian terminal, enter:
```
cd /home/pi/git/TouchSelfie/scripts
python ./photobooth_gui.py
```

Enter your gmail address, then enter your app password.
A browser window should pop-up for you to agree.
One authentication is complete, you should receive a long alpha-numeric code to be copied and pasted into the terminal.

The photobooth_gui.py should be full screen.
Click the customize button to set your AlbumID and other parameters.

At parties, run:
```
cd /home/pi/git/TouchSelfie/scripts
python ./photobooth.py
```
to prevent users from changing your parameters.
