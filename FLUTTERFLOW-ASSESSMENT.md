# FlutterFlow assessment

FlutterFlow builds Flutter apps visually. It cannot import an HTML/CSS/JavaScript website, so the screens have to be rebuilt there. What carries over is the design, content, rules and data structure.

## Reuse as is
- Brand: name, purple palette, wordmark and stack logos, welcome-screen design image, leaf background (`assets/extracted/`, `assets/design-reference/`)
- Fonts: Outfit, Figtree, Caveat, Yellowtail (all available from Google Fonts in FlutterFlow)
- Text: all screen copy, plan names and points, error messages
- Business rules, written down in code and `docs/DATA-MODEL.md`: tiers and prices, 7/30-day rules, order steps, delivery slots, dish catalogue, partner document list
- Firebase project `highway4-f3dc9` (phone sign-in is supported inside FlutterFlow)
- The flow of each screen, which you can follow from the screenshots and the code

## Adapt
- Data model: turn each `S.*` collection into a Firestore collection (field lists in `docs/DATA-MODEL.md`)
- Meal planner, price calculation, skip and pause rules: become Dart custom functions, and should also run on a server (Cloud Functions) so users cannot change them
- Roles (customer, kitchen, delivery, admin): Firebase Auth plus a role field and Firestore security rules instead of the password check in the page
- Maps: FlutterFlow has a Google Map widget; the app only used links so far

## Rebuild
- Every screen and navigation (home, search, plans wizard, taste, orders, tracking, profile, kitchen, delivery, admin, chat, partner application form)
- State handling (the single `S` object and `render()`)
- Document upload (needs Firebase Storage)
- Payments (needs a gateway; none exists today)
- Notifications, chat storage, admin approvals as real database writes

## Do not carry over
- The in-page staff passwords and codes
- The assumption that all data is in memory
