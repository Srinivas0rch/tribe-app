# tribe-app

Find Your Tribe - README

This is a live audience participation app for your AI Academy event.
Students scan a QR code, answer 5 questions, and AI groups them into one of 5 tribes.
The results show live on your presenter screen.

---

LINKS

Student form   : tribe-app-self.vercel.app/form
Dashboard      : tribe-app-self.vercel.app/dashboard
Firebase       : console.firebase.google.com
Vercel         : vercel.com/dashboard

---

FILES IN THIS PROJECT

form.html       - The page students open on their phones
dashboard.html  - The page you display on the projector
vercel.json     - Tells Vercel to serve clean URLs without .html

---

BEFORE THE EVENT

1. Go to console.firebase.google.com
2. Open the find-your-tribe project
3. Click Realtime Database in the left menu
4. Hover over the responses node and click the trash icon to delete all test data
5. Open the dashboard URL on your laptop and confirm it shows 0 responses
6. Connect your laptop to the projector

---

ON THE DAY

1. Open dashboard on your laptop and keep it on the projector screen
2. Show the QR code to students on your opening slide
3. Wait for responses to come in - you will see the counter go up live
4. When enough students have responded, click the Show AI Clustering button
5. Walk the audience through the tribe bubble map on screen

---

AFTER THE EVENT

1. Go to Firebase console
2. Click Realtime Database, then the Rules tab
3. Change both .read and .write from true to false
4. Click Publish to lock the database

---

THE 5 TRIBES

Night Owls      - Creative, late-night thinkers
Dream Builders  - Ambitious, goal-oriented
Quiet Rebels    - Introverted but original
Fire Starters   - High energy, social, extroverted
Free Spirits    - Curious, flexible, open to anything

---

IF SOMETHING BREAKS

Problem: Dashboard shows no data
Fix: Check your internet connection. Refresh the page.

Problem: Students cannot open the form
Fix: Make sure the venue WiFi is working. Ask students to use mobile data if needed.

Problem: Vercel shows 404
Fix: Make sure you are going to /form or /dashboard, not just the root URL.

Problem: Need to reset data during the event
Fix: Go to Firebase, delete the responses node, refresh the dashboard.

---

TECH USED

Firebase Realtime Database  - stores student responses live
Vercel                      - hosts the two HTML pages for free
K-means clustering          - groups students into tribes, runs in the browser, no API needed
