# Scouting-App by Darmik N, Amal E, and Rahul T


# FRC 2026 — Rebuilt Scout Tracker

A scouting app for FRC teams. Log match data, then see ranked charts and
per-stat leaderboards to help decide which teams to pick.

Built with **Python + Flask**, **matplotlib** for charts, **Bootstrap** for
styling, and a plain **CSV file** for storage (no database, no JSON).

---

## What you need before starting

- **Python 3.8 or newer** (the installer is below)
- The two Python libraries the app uses: **Flask** and **matplotlib**
  (installed automatically in Step 5 — you do not download these by hand)
- An **internet connection the first time** (to install the libraries and to
  load the page styling)

---

## Setup — from a brand-new computer

The steps are the same on Mac and Windows. Where they differ, both are shown.

### 1. Install Python

Go to **https://python.org/downloads** and click the big **Download Python**
button, then run the installer.

- **Windows — IMPORTANT:** on the first installer screen, check the box
  **"Add Python to PATH"** at the bottom *before* clicking Install.
  If you skip this, none of the commands below will work.
- **Mac:** just click through (Continue → Agree → Install).

To confirm it worked, open a terminal (see Step 3) and run:

```bash
python3 --version     # Mac
python --version      # Windows
```

You should see something like `Python 3.11.5`.

### 2. Get the app files

1. Download **`frc_scouting.zip`**.
2. Find it in your **Downloads** folder and extract it:
   - **Mac:** double-click the zip.
   - **Windows:** right-click → **Extract All → Extract**.
3. You now have a **`frc_scouting`** folder.

### 3. Open a terminal

- **Mac:** press **Cmd + Space**, type **Terminal**, press Enter.
- **Windows:** press the **Windows key**, type **PowerShell**, press Enter.

### 4. Move into the project folder

```bash
cd ~/Downloads/frc_scouting     # Mac
cd ~\Downloads\frc_scouting     # Windows
```

*(The only difference is the slash direction.)*

### 5. Install Flask and matplotlib

This single command reads `requirements.txt` and installs **both** Flask and
matplotlib for you:

```bash
pip3 install -r requirements.txt     # Mac
pip install -r requirements.txt      # Windows
```

Wait for it to finish.

> **If that command fails**, install the two libraries directly instead:
> ```bash
> pip3 install Flask matplotlib      # Mac
> pip install Flask matplotlib       # Windows
> ```

### 6. Start the app

```bash
python3 app.py     # Mac
python app.py      # Windows
```

You'll see a line like:

```
* Running on http://127.0.0.1:5001
```

That means it's working. **Leave this terminal window open** — closing it
stops the app.

### 7. Open it in your browser

Go to:

```
http://localhost:5001
```

---

## Using the app

The app starts with **no data**, but if you want premade data, download **scouting_data.csv** and move it into the data folder inside of the frc_scouting folder. There are three tabs:

- **Scouting Form** — log one match at a time (team, match #, balls scored,
  defense/speed/climb ratings). Click **Submit Entry** to save.
- **Data Analysis** — pick a stat under **"Rank teams by"** and every team is
  ranked best-to-worst (with a podium), plus a radar comparison and a
  "Best in Each Category" leaderboard. Use **"Show stats"** to hide stats you
  don't care about.
- **Admin** — data summary and cleanup tools (delete one entry, remove
  duplicates, or **Fix Out-of-Range Values** to correct impossible numbers
  without deleting anything).

---

## Everyday use (after the first setup)

You only install things once. To run the app again later:

1. Open a terminal.
2. `cd` into the folder (Step 4).
3. Run the start command (Step 6).

To **stop** the app: click the terminal and press **Ctrl + C**.

---

## Troubleshooting

| Problem | Fix |
|---|---|
| `command not found: python3` / `pip3` (Mac) | Use `python` and `pip` instead |
| `python is not recognized` (Windows) | Python wasn't added to PATH — reinstall and check the **"Add Python to PATH"** box |
| `ModuleNotFoundError: No module named 'flask'` (or `matplotlib`) | The install step didn't run — repeat Step 5, or use the direct-install fallback |
| `Address already in use` on 5001 | An old copy is probably still running — close that terminal, or change `port=5001` to `5002` at the bottom of `app.py` |
| Page loads but looks unstyled | Needs internet the first time (it loads Bootstrap + fonts from the web) |

---

## Keeping your data

Your scouting entries are saved in **`data/scouting_data.csv`** inside the
project folder. To move your data to another computer, copy that one file into
the new computer's `data/` folder. A fresh download starts empty.
