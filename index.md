Config for the UI
 
---

*API Endpoints*

+ "Where does my data come from?"
+ Static per environment
+ Can store values in SSM

<div data-background-image='./table.png'></div>
---

*Auth Info*

+ Client pool / id
+ Static per environment
+ Can store values in SSM

---

*Application Options*

+ List of Sensors
+ Basemaps
+ min/max Map zoom
+ etc.

---

*Branding*

+ Background image
+ Title bar logo / text
+ Per-app branding (Inmarsat demo)
+ Per-org branding(?)

---

*Feature Toggles* AKA *App-specific permissions*

+ A/B Testing
+ What apps can this user use? 
  - SSO Homepage
  - Channels &rarr; EventExplorer?

---

*Proposal:* UI Config Service

<div data-background-image='./table.png'></div>
---

+ Dockerized
+ Lives in the fe cluster
+ Uses AWS SDK for talking to s3 and SSM

---

*Public Endpoints*

+ Get config for initial app load
+ Get full configs for authenticated users
+ [FUTURE] Access limited UI for select power-users (Apex)

---

*Private Endpoints* (VPN-only)

+ Access full UI for customizing config values

<div data-background-image='./seq-diag.png'></div>
<div data-background-image='./onion.png'></div>
---

We will make sure the UI indicates very clearly which fields have their default values, and which fields are being overwritten at the app, org, and user levels. 

---
Fight me
---

