# Herbs House

Mobile-friendly front door website for Herbs House — Ballard's original medically endorsed herbs. Est. 2013.

## Live Site

https://herbs-house.onrender.com/

## Tech Stack

- **Backend**: Python Flask
- **Server**: Gunicorn (production)
- **Hosting**: Render (auto-deploys from `main`)
- **Python**: 3.12

## Project Structure

```
herbs-house/
  app.py              # Flask app — serves index.html and static assets
  index.html          # Main landing page
  requirements.txt    # Python dependencies (Flask, Gunicorn)
  .python-version     # Pins Python 3.12 for Render
  html/image/         # Static images (logo, splash)
  video/              # MP4 video files (autoplay, looping)
```

## Setting Up the Development Environment on Windows 11

### Prerequisites

1. **Install Python 3.12**
   - Download Python 3.12 from https://www.python.org/downloads/
   - During installation, check **"Add Python to PATH"**
   - Verify installation by opening a terminal:
     ```
     python --version
     ```
     You should see `Python 3.12.x`

2. **Install Git**
   - Download Git from https://git-scm.com/download/win
   - Run the installer with default settings
   - Verify installation:
     ```
     git --version
     ```

### Clone the Repository

Open a terminal (Command Prompt, PowerShell, or Git Bash) and run:

```
cd C:\Users\%USERNAME%\Projects
git clone https://github.com/nbk5876/herbs-house.git
cd herbs-house
```

If the `Projects` folder doesn't exist, create it first:

```
mkdir C:\Users\%USERNAME%\Projects
```

### Create a Virtual Environment

```
python -m venv venv
```

Activate the virtual environment:

- **Command Prompt:**
  ```
  venv\Scripts\activate
  ```
- **PowerShell:**
  ```
  venv\Scripts\Activate.ps1
  ```
- **Git Bash:**
  ```
  source venv/Scripts/activate
  ```

You should see `(venv)` at the beginning of your prompt.

### Install Dependencies

```
pip install -r requirements.txt
```

### Run the App Locally

```
python app.py
```

Open your browser and visit http://localhost:5000

The site will load with the homepage, images, and videos. Press `Ctrl+C` in the terminal to stop the server.

### Making Changes

1. Edit files (e.g., `index.html` for content, `app.py` for routes)
2. Refresh the browser to see changes (restart the server if you changed `app.py`)
3. When ready to deploy:
   ```
   git add .
   git commit -m "description of changes"
   git push origin main
   ```
   Render will auto-deploy within a few seconds of the push.

## Deployment

Push to `main` triggers auto-deploy on Render. Start command: `gunicorn app:app`

## Location

716 NW 65th St, Seattle, WA 98117
