# StatifyPlus 🎵

StatifyPlus is a web application that gives you detailed insights into your Spotify listening habits. View your top artists, top tracks, and currently playing song — all in a clean and modern interface powered by the Spotify Web API.

## Features

- **Spotify OAuth Login** — Secure authentication via Spotify's official OAuth 2.0 flow
- **Top Tracks** — Browse your 50 most listened tracks across three time ranges (last 4 weeks, 6 months, all time)
- **Top Artists** — Discover your 50 most played artists with the same time range filters
- **Home Dashboard** — Quick overview of your top 3 tracks and artists at a glance
- **Now Playing** — See what's currently playing on your Spotify account
- **Session Management** — Automatic session expiry and secure logout
- **Custom 404 Page** — Friendly error page for unknown routes

## Tech Stack

- **Backend:** Python / Flask
- **Authentication:** Spotify OAuth 2.0
- **API:** Spotify Web API
- **Frontend:** HTML, CSS, JavaScript (Vanilla)
- **Environment:** python-dotenv

## Installation

### Prerequisites

- [Python 3.7+](https://www.python.org/downloads/)
- A [Spotify Developer Account](https://developer.spotify.com/)

### Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/ismetcelenler/Stats-for-Spotify.git
   cd Stats-for-Spotify
   ```

2. **Set up a virtual environment** (optional but recommended):
   ```bash
   python -m venv venv
   venv\Scripts\activate       # Windows
   # source venv/bin/activate  # macOS / Linux
   ```

3. **Install dependencies:**
   ```bash
   pip install -r Requirements.txt
   ```

4. **Set up your Spotify API credentials:**
   - Go to the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/)
   - Click **Create app** and fill in the details
   - Add `http://127.0.0.1:8888/callback` as a **Redirect URI** and hit **Save**
   - Copy your **Client ID** and **Client Secret**

5. **Create a `.env` file** in the project root:
   ```env
   CLIENT_ID=your_spotify_client_id
   CLIENT_SECRET=your_spotify_client_secret
   SECRET_KEY=your_random_secret_key
   REDIRECT_URI=http://127.0.0.1:8888/callback
   ```
   > You can copy `.env.example` as a starting point.

6. **Run the application:**
   ```bash
   python App.py
   ```

7. Open your browser and navigate to **[http://127.0.0.1:8888](http://127.0.0.1:8888)**

## Usage

1. Click **Login with Spotify** on the welcome page
2. Authorize the app to access your Spotify data
3. Explore your top tracks and artists using the time range filters:
   - **Last 4 Weeks**
   - **Last 6 Months**
   - **All Time**

## Project Structure

```
Stats-for-Spotify/
├── App.py                  # Main Flask application
├── Requirements.txt        # Python dependencies
├── .env                    # Environment variables (not committed)
├── .env.example            # Example environment file
├── static/
│   ├── main.css
│   ├── main.js
│   ├── style.css
│   ├── top-tracks.css
│   ├── top-tracks.js
│   ├── top-artists.css
│   ├── top-artists.js
│   ├── callback.css
│   └── icons/
└── templates/
    ├── welcome.html
    ├── main.html
    ├── top_tracks.html
    ├── top_artists.html
    ├── callback.html
    └── not_found_404.html
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [Spotify Web API](https://developer.spotify.com/documentation/web-api/)
- [Flask](https://flask.palletsprojects.com/)
