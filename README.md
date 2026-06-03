# Scouting-App
Here are the combined setup instructions again, now with the port as 5001.

Running the FRC Scouting App
1. Install Python
Go to python.org/downloads and click the big "Download Python" button. Run the installer.

Windows only — important: on the first installer screen, check "Add Python to PATH" at the bottom before clicking Install. Skipping this breaks every command below.
Mac: just click through (Continue → Agree → Install).

2. Get the app files
Download frc_scouting.zip, then find it in your Downloads folder and extract it:

Mac: double-click the zip.
Windows: right-click → Extract All → Extract.

You'll get a frc_scouting folder.
3. Open the terminal

Mac: press Cmd + Space, type Terminal, press Enter.
Windows: press the Windows key, type PowerShell, press Enter.

4. Go into the folder

Mac: cd ~/Downloads/frc_scouting
Windows: cd ~\Downloads\frc_scouting

(The only difference is the slash direction.)
5. Install the app's two libraries

Mac: pip3 install -r requirements.txt
Windows: pip install -r requirements.txt

Wait for it to finish — 30–60 seconds of text scrolling. (Needs internet.)
6. Start the app

Mac: python3 app.py
Windows: python app.py

You'll see a line like Running on http://127.0.0.1:5001. Leave this window open — closing it stops the app.
7. Open it in a browser
Go to http://localhost:5001

Once it's running

The app starts with no data. Use the Scouting Form tab to add a few entries, then check Data Analysis.
You can also download the scouting_data.csv and drag it into the "data" folder inside of the folder created by extracting the zip file.
Stop the app: click the terminal and press Ctrl + C.
Run it again later: nothing to reinstall — just open the terminal, do step 4 (cd into the folder), and step 6 (start command).


