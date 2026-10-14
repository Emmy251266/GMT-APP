GMT CHURCH APP  (separate project, not part of the website)
==========================================================

FILES
  index.html            the whole app
  manifest.webmanifest  app name, colours, icon
  sw.js                 offline helper

HOST IT (free)
  1. Create a NEW project on Vercel (or Netlify) and upload this folder.
     It is its own site, with its own address (e.g. gmt-app.vercel.app).
  2. Open that address on a phone and test: create an account, log in.

SUPABASE (needed once)
  Authentication > URL Configuration:
    - add the new app address under "Redirect URLs"
  In index.html, set APP_URL to the app address (near the top of the script),
  so password-reset emails come back to the app.

MAKE THE APK
  1. Go to pwabuilder.com, paste the app address, press Start.
  2. Package for stores > Android > Generate.
  3. The zip has a test .apk (install on a phone) and an .aab (for Google Play).
  Keep the signing key file safe. You need it for every update.

ICON
  The icon and splash images load from the church website. For the best
  result put a square 512x512 PNG of the logo in this folder and change the
  "src" in manifest.webmanifest to its file name.
