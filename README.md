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

## Local Development

```bash
pip install -r requirements.txt
python app.py
```

Visit http://localhost:5000

## Deployment

Push to `main` triggers auto-deploy on Render. Start command: `gunicorn app:app`

## Location

716 NW 65th St, Seattle, WA 98117
