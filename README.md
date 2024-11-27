## Overhead

A simple demo web app designed to tell you what flights are directly overhead.

### Setup

Copy `private_keys_template.py` to `private_keys.py` and fill in with your own details. (Skip this step if you don't have the API keys)

`pip install -r requirements.txt` to download the required packages

### To run

`FLASK_ENV=app flask run`

or

`python -m flask run`

Will run the app on localhost:5000.

## What it does

Displays local planes in the air and (if unmuted) plays a sound whenever a plane is directly overhead, so you can quickly identify it.

## How it does it

This flask/JS app queries the OpenSky [REST API](https://opensky-network.org/apidoc/rest.html) for local flight information using location information returned by [IPStack](https://ipstack.com/). If the user gives permission, the page instead uses HTML5 geolocation for much more accurate location info. It generates a map using leaflet.js and [MapBox](https://www.mapbox.com/).

This is only meant to be run locally, for your own amusement. You must update `private_keys.py` with your own API keys for these services to work. (Skip this if you don't have the API keys)

![screenshot](assets/screenshot.png)