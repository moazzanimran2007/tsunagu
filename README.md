# つなぐ Tsunagu

Tsunagu is a prototype from the Kyoto AI Innovation Lab, built for the Elderly Connection and Mimamori challenge track. It helps older residents in Kyoto find local community events. They can register themselves, or a family member or local supporter can register them. Organizers post events, and a recommendation engine picks a few nearby events for each person. Those suggestions are delivered by phone call or in a simple large-text screen.

All people, organizers and events in the prototype are sample data.

## Run it

It's one file. Open `index.html` in a browser, or publish the repo with GitHub Pages (Settings → Pages → Deploy from branch → `main` / root).

## What's in it

- **Older adult view.** Large text with an adjustable size. It shows three suggestions a week, each with when, where, how to get there, cost and why it was picked. The person taps "I'd like to go" or "Please call me about this".
- **Registration.** One question per screen, for a person registering themselves, a family member, or a community supporter (e.g. a 民生委員 / welfare volunteer).
- **Family / supporter dashboard.** Manage profiles, see suggestions and sign-ups, and send a suggestion by phone.
- **Organizer portal.** Post one-off, weekly or monthly events, with helping-role and cross-generational flags.
- **Staff view.** A call queue with a simulated call: the script is read aloud with browser text-to-speech and the outcome is recorded. Also moderation and reports.
- **Recommendations.** Rule-based scoring on interests, distance, available times, accessibility, helping roles and past declines, with a limit of two suggestions per category. An optional AI layer re-ranks the picks and writes call scripts. It only runs when the page is opened as a Claude artifact; elsewhere the rules and template scripts are used.
- **Spam safeguards.** Individual organizers need approval and can post 3 events a week. Events with links, requests for personal info or payment, or high fees are held for review.

Demo data is kept in the browser's localStorage. Use "Reset demo data" in the footer to start over.

## Not yet built

- Real telephony or a voice-agent provider. The call logic is kept in one place so a provider can be added later.
- A shared backend. Each browser has its own copy of the data.
