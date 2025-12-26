# Song Lyrics Generator

Song Lyrics Generator is a Flask-based web application that generates Hindi song lyrics (written in English text) using the Google Generative Language API. The application provides a simple web interface where users can enter a prompt, submit it, and receive AI-generated song lyrics displayed on a results page.

The project focuses on simplicity, browser usability, and safe content generation with logging for debugging.

---

## Overview

The application includes:

* A Flask backend with routing for home and lyrics generation.
* Integration with Google Generative Language API (Gemini-Pro).
* Basic safety validation to filter high-risk content.
* Frontend templates for input and output views.
* Static stylesheet for UI styling.
* Logging enabled for debugging and API response tracing.

---

## Features

* Home page with lyrics generator input form
* Song lyrics generation using external API
* Safety rating validation before displaying lyrics
* Responsive results page displaying generated lyrics
* Custom CSS styling
* Debug logging in application
* Gunicorn support for deployment

---

## Tech Stack

* **Backend:** Flask
* **HTTP Client:** Requests
* **Templating:** Jinja2
* **Frontend:** HTML, CSS
* **Logging:** Python logging module
* **Deployment Ready:** Gunicorn

Dependencies are listed in `requirements.txt`.

---

## Project Structure

```
Song-Lyrics-Generator-main/
│
├── app.py                     # Main Flask application
├── requirements.txt           # Dependencies
│
├── templates/
│   ├── index.html             # Home page with prompt form
│   └── result.html            # Lyrics display page
│
└── static/
    └── styles.css             # Styling
```

---

## Installation

1. Ensure Python is installed.
2. Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Running the Application

Start the Flask application:

```bash
python app.py
```

The application runs in debug mode and is typically available at:

```
http://127.0.0.1:5000/
```

---

## Usage

1. Open the application in your browser.
2. Enter a song lyrics prompt.
3. Submit the form.
4. View generated lyrics on the results page.

---

## API Integration

* Uses:

  ```
  https://generativelanguage.googleapis.com/v1beta/models/gemini-pro:generateContent
  ```
* API key usage is defined in `app.py`.

---

## Notes

* Default lyrics style is Hindi lyrics written in English text.
* Unsafe results are blocked based on safety ratings.
* Logging is enabled for debugging.
* Static assets are served via Flask.

---

## License

No license file is included in this project.
