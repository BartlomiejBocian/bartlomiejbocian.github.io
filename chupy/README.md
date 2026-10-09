# Chupy privacy page

This folder is ready to copy into the root of
`BartlomiejBocian/bartlomiejbocian.github.io` as `chupy/`.
The only website file needed is `chupy/privacy.html`; no build step, packages,
scripts, external fonts, or additional assets are required.

## Before publishing

- Confirm the developer name **Bartłomiej Bocian** and contact email
  **old.stoork@gmail.com**. These match the existing CardVault privacy page.
- Confirm Chupy's intended audience. The draft does not assume an age limit or
  claim that the game is not directed at children. The current advertising
  implementation supports a confirmed general audience only; children or a
  mixed audience need a separate implementation and policy review.
- Review support-message retention, the applicable legal bases, and any
  additional controller details required for your jurisdiction. This page
  describes the implemented app and Google's documented practices; it is not
  a legal determination of compliance.
- Check the update date against the date you publish the policy.

## Publish with GitHub Pages

1. Copy `privacy.html` to `chupy/privacy.html` in the existing website checkout:
   `/Users/bartlomiejbocian/Developer/GitHub/bartlomiejbocian.github.io`.
   Do not replace the existing CardVault pages.
2. Commit and push that new file to the website repository's `main` branch.
   Its existing GitHub Pages deployment serves files from the repository root.
3. Wait for the `pages-build-deployment` workflow to finish successfully, then
   verify this URL opens without signing in:

   **https://bartlomiejbocian.github.io/chupy/privacy.html**

4. Use that same public URL in App Store Connect's Privacy Policy URL, AdMob's
   Privacy & messaging configuration, and the Choopy app target's Release
   `CHOOPY_PRIVACY_POLICY_URL` build setting. Do not use the GitHub repository
   or `blob/main` URL.
5. Set Release `CHOOPY_ADS_AUDIENCE` to `general` only after confirming that
   audience. AdMob app/unit IDs are already configured; publishing this page
   alone does not enable production ads. Follow `Documentation/RewardedAds.md`
   in the game repository for the remaining production checks.

The page has been prepared locally; nothing has been pushed or published.
The app's policy URL remains unset until the public page exists, avoiding a
broken link in Settings.

## Preview locally

From the parent `Developer/GitHub` directory, run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open `http://127.0.0.1:8000/chupy/privacy.html`. Check narrow and wide screens,
light and dark appearance, keyboard focus, contact links, and the policy text.

Preparation checks passed for heading structure, unique IDs, accessible section
labels, local links, HTTPS external links, and absence of scripts or remote
assets. A browser was unavailable in this session, so visual preview remains
to be checked before publication.
