# Hubertus Prep — public App Store pages

Static Polish support and privacy pages. No build step, packages, third-party assets, scripts, analytics, forms or custom cookies. `icon.png` copies the app's current bundled icon.

## Published URLs

The deployment target is `https://bartlomiejbocian.github.io/hubertusprep/`:

- App Store Connect **Support URL**: `https://bartlomiejbocian.github.io/hubertusprep/`
- App Store Connect **Privacy Policy URL**: `https://bartlomiejbocian.github.io/hubertusprep/privacy.html`
- The optional marketing URL can use the support homepage, although no separate marketing site is needed.
- Support address: `old.stoork@gmail.com`

Publish these files at `hubertusprep/` in `BartlomiejBocian/bartlomiejbocian.github.io`, on its `main` branch. That repository already serves its root through GitHub Pages. Copy only this folder, commit and push it; preserve the existing CardVault and Choopy pages. After deployment, verify both URLs above return HTTP 200. The app's `AppSupport` URLs must match the public pages.

For a local preview, run `python3 -m http.server 8080 --directory Website/hubertusprep` from the mobile repository root, then open `http://localhost:8080/` and `/privacy.html`. Check narrow and wide screens, the device's light and dark appearance, keyboard focus, the e-mail address, and both App Store URLs after deployment. Do not send test mail automatically.

## Keep the policy accurate

Before shipping a change to accounts, networking, cloud sync, advertisements, analytics, diagnostics, data storage, permissions, support providers or website hosting:

1. Recheck the implemented data flow, including SDK behavior and voluntary support messages.
2. Update `privacy.html`, its date and the support instructions when affected. Do not describe planned functionality as already implemented.
3. Review App Store Connect privacy disclosures against the actual release and Apple's current definitions.
4. Publish and verify the public HTTPS pages before pointing a release at them.

History and reading progress currently stay on the device. There is no application server, account system, ad SDK or analytics SDK. Support is voluntary e-mail through Gmail; the user reviews and sends any question report. GitHub Pages has its own technical/security logging. The privacy page distinguishes these cases rather than claiming no data can ever leave the device.

Official references checked for this version:

- [Apple: manage app privacy](https://developer.apple.com/help/app-store-connect/manage-app-information/manage-app-privacy)
- [Apple: platform version information](https://developer.apple.com/help/app-store-connect/reference/app-information/platform-version-information)
- [GitHub Pages and IP security logging](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages)
- [GitHub privacy statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement)
- [Google privacy policy](https://policies.google.com/privacy)
- [Apple: iCloud backup](https://support.apple.com/en-us/108770)
