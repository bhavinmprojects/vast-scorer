# Vastu Floor Plan Scorer

Upload a house floor plan, outline the house, tag each room and the front door, and score every facing (8 directions) and garage side against common Vastu Shastra placement rules. Lakeview Homes' Windsor model is included as a worked example.

## How it runs
- `server.js` is a small Express server that serves `public/index.html` and a health check at `/api/health`.
- Everything else runs in the visitor's browser. Uploaded plans are stored in that browser only (localStorage) and never reach the server.
- No API key or environment variables are needed.
- PDF uploads use pdf.js, loaded from cdnjs when a PDF is chosen.

## Deploy on Render
1. Push this folder to a GitHub repository (keep `index.html` inside `public`).
2. In Render choose New, then Web Service, and pick the repository.
3. Build command `npm install`, start command `npm start`, instance type Free.
4. Open `https://<your-app>.onrender.com/api/health` and confirm `{"ok":true}`.

`render.yaml` describes the same settings if you'd rather use Render's Blueprint option.

## Run locally
```
npm install
npm start
```
Then open http://localhost:3000.

## Limits
This is a screening tool. Rules follow consensus across published Vastu sources (listed in the app), room zoning uses the room centre against an 8-direction grid, and pada numbering is indicative. Have a Vastu consultant review a specific lot before signing.
