# Fish Tank: clickable v1

A one-file prototype of Fish Tank, an app where people pitch a business by video and get backers, mentors and help. It runs in any browser with no build step. All people and numbers in it are sample data, and no real money moves.

## Run it

Open `index.html` in a browser.

## Put it online

- **Vercel:** import this repository, set the root directory to `fishtank-app`, and deploy with no framework preset.
- **Netlify or GitHub Pages:** serve the `fishtank-app` folder as a static site.

## What's inside (V2)

One welcome flow, then a separate app for each kind of user:

- **Business app** (teal): a 5-step journey, a pitch builder with one question per screen and a live Fish Score, a pitch status page, and help (mentors, government schemes, guides).
- **Investor app** (gold): a feed of verified businesses with risk levels and returns in plain words ("put ₹10,000, get ₹347 a month"), a pitch page with proof and questions, an invest flow with RBI limits and consent, a portfolio, and a "before you invest" guide.
- **Helper app** (plum): mentors get requests, earnings and a profile; franchise brands and lenders get a candidate pipeline and a listing.
- **Just looking**: a read-only investor feed that asks the visitor to sign up.

On a computer the app shows in a phone frame, with a presenter panel to switch between users. On a phone it runs full screen. The welcome flow and menus are in English, Hindi and Telugu.
