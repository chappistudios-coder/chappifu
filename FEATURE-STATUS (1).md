# Feature status

How this was checked: the business logic was run in Node with `tests/logic-smoke-test.js` (fake DOM, in-memory). Screens were rendered with the same fake DOM to see that nothing throws. **No screen was opened in a real browser or phone, and no SMS was sent.** Anything not in the first two groups is untested.

## 1. Logic verified by the test (works inside one session)
- Customer sign-up and login by phone number (the app side), duplicate numbers blocked, unknown numbers blocked
- Kitchen application submit, admin approval creating a kitchen with dishes
- Nearby kitchen list
- 7-day and 30-day subscription creation and price calculation
- Next-day meal planning
- Skip limit (7-day plan: 1), pause blocked on 7-day plans
- Kitchen 7-day menu plan and customer extras picks (roti, chawal, dal) counted per day
- One-time order placement, order step rules, admin statistics

## 2. Screens that rendered without error (not visually checked)
Customer Home, Search, Plans, My Taste, Orders, Profile; Welcome, Login, Sign-up, Staff sign-in.

## 3. Written but NOT verified
- **Firebase phone OTP**: the code and your project settings are in, but no SMS was sent. Needs Phone sign-in enabled and the site added to authorized domains
- Kitchen, delivery and admin panels as screens; chat; document uploads; ratings, complaints, refunds, notifications
- Location detection (browser geolocation) and the Google Maps links
- Light theme, theme switch
- The Android APK workflow (last built result is unknown to me)

## 4. UI only / not real yet
- **Payments**: a record is stored; there is no payment gateway
- **Staff sign-in**: compares a password written in the page; no staff accounts exist now. Not secure for production
- **Saving data**: nothing is stored on a server or in the browser (except theme). Reload loses everything
- Prices, limits and approvals are all decided in the browser; a server would have to repeat them
