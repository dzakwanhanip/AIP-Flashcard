# Malaysia AIP Flash Cards

A study and quiz web app for air traffic controllers, built from the public Malaysian AIP (https://aip.caam.gov.my).

Live site: https://dzakwanhanip.github.io/AIP-Flashcard/

## How it works

The whole app is one file, `index.html`. It runs in any browser on phones and computers, and needs no server.

- **Study** mode: flip cards, mark them "Got it" or "Again". Progress is saved in each user's own browser.
- **Quiz** mode: 10 multiple-choice questions from the chosen deck, with a best score per deck.

## Editing cards

Cards are in the `CARDS` list near the bottom of `index.html`. Each card looks like this:

```js
{ part: "ENR", v: 1, ref: "ENR 1.7.1.2", q: "Transition altitude?", a: "11 000 ft", w: ["13 000 ft", "10 000 ft", "11 500 ft"] },
```

- `part`: GEN, ENR or AD (which deck it appears in)
- `v: 1`: the card has been checked against the AIRAC issue named in `AIRAC` in the file
- `ref`: the AIP paragraph the answer comes from
- `w`: believable wrong answers; the quiz shows two of them plus one obviously wrong answer from another card
- `g` (optional): a group name; only used for quiz wrong answers if a card has no `w`
- `q` / `a`: question and answer

## Accuracy

ENR cards (focused on the Kota Kinabalu FIR) are based on AIRAC AIP AMDT 04/26 (effective 29 OCT 2026). GEN and AD cards are unchecked samples.
Always refer to the current AIP. This is a study aid only, not for operational use.

## Version numbers

The version at the bottom of the app is written as MAJOR.MINOR.PATCH, for example 1.4.0.

- PATCH (last number) goes up for card corrections and small fixes.
- MINOR (middle number) goes up when a new feature is added; PATCH resets to 0.
- MAJOR (first number) goes up only for a big change, such as adding accounts.

History:

- 1.5.1 (29 Oct 2026): Counter line shows 0 instead of hiding when one count has no data yet.
- 1.5.0 (29 Oct 2026): Anonymous usage counter (GoatCounter account "aipflashcard"): counts study sessions and completed quizzes.
- 1.4.0 (29 Oct 2026): Back and Next buttons in Study mode; new version numbers.
- 1.3.0: Quiz no longer repeats questions until the whole deck has been used.
- 1.2.0: Abbreviation explanations, ATS hours cards, Kota Kinabalu RNP Z RWY 20 chart cards.
- 1.1.0: Flag this answer (Google Form).
- 1.0.0 (28 Oct 2026): First release with Study and Quiz modes.
