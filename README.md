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
{ part: "ENR", v: 1, ref: "ENR 1.7.1.2", g: "alt", q: "Transition altitude?", a: "11 000 ft" },
```

- `part`: GEN, ENR or AD (which deck it appears in)
- `v: 1`: the card has been checked against the AIRAC issue named in `AIRAC` in the file
- `ref`: the AIP paragraph the answer comes from
- `g` (optional): a group name; quiz wrong answers are picked from cards in the same group
- `q` / `a`: question and answer

## Accuracy

ENR cards are based on AIRAC AIP AMDT 04/26 (effective 29 OCT 2026). GEN and AD cards are unchecked samples.
Always refer to the current AIP. This is a study aid only, not for operational use.
