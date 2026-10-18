# Project analysis

## Technology and versions (read from the files, not guessed)
| Item | Finding |
|---|---|
| App type | Single-page web app in one file, `index.html` (1,347,674 bytes at packaging time) |
| Framework | None. Plain HTML5, CSS3 and vanilla JavaScript (modern syntax: async/await, template literals, CSS variables, `:has()`, `aspect-ratio`) |
| App version | None declared |
| Build tool, bundler, package manager | None. No `package.json`, no lockfile |
| Fonts | Google Fonts, loaded online: Outfit, Figtree, Caveat, Yellowtail. Not bundled |
| Firebase | Web SDK **10.12.5** (compat build) loaded at runtime from `www.gstatic.com`. Only Firebase Authentication (phone) is used |
| Firestore, Storage, Analytics, Cloud Functions | Not used (the code contains none) |
| Maps | Only links to Google Maps (directions and search). No Maps SDK, no API key |
| Android build | GitHub Actions: Node 20, Java 17, Capacitor **6**. The APK opens the live website in a WebView |
| Backend, API routes, SQL | None. The code makes no `fetch` or XMLHttpRequest calls |
| Storage in the browser | Only the light/dark theme (`localStorage` key `hw-theme`) |

## How the code is organised (inside the one `<script>`)
Data and rules (`emptyData`, `TIERS`, `RULES`, `CAT`, `DOC_DEFS`) > pricing and meal planner (`planPrice`, `planTomorrow`, `bookTomorrow`, `recommend`) > orders and subscriptions (`placeOrder`, `makeOrder`, `subscribe`, `subAction`) > accounts and applications (`signUpWithOtp`, `loginWithOtp`, `staffLogin`, `submitApplication`, `activateKitchen`, `activateRider`) > Firebase OTP (`fbLoad`, `fbSend`, `fbVerify`) > screens (customer, kitchen, delivery, admin, chat) > click and input handlers (objects `H` and `HI`) > `render()` and `boot()`.

## Roles in the app
Customer, kitchen partner, delivery partner, admin. Partners apply in the app; the admin approves; approval creates the kitchen or rider.

## Embedded images
- `assets/extracted/01-fol.svg` (image/svg+xml, 12 KB)
- `assets/extracted/02-fol-sm.svg` (image/svg+xml, 8 KB)
- `assets/extracted/03-sprig.svg` (image/svg+xml, 5 KB)
- `assets/extracted/04-blossom.svg` (image/svg+xml, 10 KB)
- `assets/extracted/05-gleaf.svg` (image/svg+xml, 0 KB)
- `assets/extracted/06-wave.svg` (image/svg+xml, 0 KB)
- `assets/extracted/07-wave-d.svg` (image/svg+xml, 0 KB)
- `assets/extracted/08-pat.svg` (image/svg+xml, 1 KB)
- `assets/extracted/09-pat-d.svg` (image/svg+xml, 1 KB)
- `assets/extracted/10-photo.jpg` (image/jpeg, 33 KB)
- `assets/extracted/11-leaves-background.jpg` (image/jpeg, 79 KB)
- `assets/extracted/12-embedded.jpg` (image/jpeg, 213 KB)
- `assets/extracted/13-logo_mark.png` (image/png, 25 KB)
- `assets/extracted/14-logo_word.png` (image/png, 114 KB)
- `assets/extracted/15-logo_stack.png` (image/png, 335 KB)
