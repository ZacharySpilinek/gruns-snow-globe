# Snow Globe

A single-page snow globe in one self-contained HTML file (`snow-globe-standalone.html`), with no build step and no dependencies.

- **Desktop:** shrink the browser window and drag it around to shake the snow, or fling the globe with your mouse.
- **Phone:** tap **Use phone motion**, then tilt or shake the phone.

## Run locally

From this folder:

```sh
python3 -m http.server 8000
```

Open http://localhost:8000/snow-globe-standalone.html

## Test on a phone (ngrok)

Phone motion sensors only work over HTTPS, so use ngrok to get an HTTPS URL.

1. Install ngrok and add your auth token (one time):
   ```sh
   brew install ngrok
   ngrok config add-authtoken <your-token>   # from dashboard.ngrok.com
   ```
2. With the local server above still running, in a second terminal:
   ```sh
   ngrok http 8000
   ```
3. On your phone, open the `https://….ngrok-free.app` URL it prints, followed by `/snow-globe-standalone.html`.
4. If ngrok shows a warning page, tap **Visit Site**.
5. Tap **Use phone motion** and allow access when asked (iOS asks every time).
