# Self-Booking HubSpot Walkthrough

An interactive training simulator that walks Wall Street English sales staff through the
HubSpot standard operating procedure (SOP) for handling **self-booked appointments** —
from spotting the appointment in the calendar to updating the deal after the consultation.

## Purpose

This is a hands-on, click-through trainer. Instead of reading the SOP, staff practise the
exact workflow in a safe, simulated "HubSpot Sandbox" environment. Each step must be
completed correctly before the next one unlocks, so trainees finish having performed every
action in order.

## How to use

1. Open `index.html` directly in any modern web browser — double-click the file or drag it
   into a browser tab.
2. No installation, server, or build step is required.
3. Work through the five steps in order. Each step gates the next, and a progress bar and
   task checklist track how far you've got.

## The five steps

1. **Calendar Check** — Identify a self-booked appointment in Outlook and learn about buffer
   time and blocking. Includes a multiple-choice quiz.
2. **Find the Deal** — Open HubSpot Deals, apply an advanced filter on "Booking Source", and
   locate the correct deal card.
3. **Review Contact** — Inspect the contact record across its Overview, Activities, and
   Intelligence tabs, then answer a signal question about the best opener.
4. **Post-Appointment Update** — Set the meeting outcome, fill in the consult notes, drag the
   deal card from "Booked" to "Open Decision", and create a follow-up task with a reminder.
5. **Complete** — Success screen with a completion code (`WSE-SB-OPEN-DECISION-2026`) to copy
   into the Knowledge Check.

## Tech & structure

- **Single-file app:** everything lives in `index.html` (~2,300 lines).
- **Vanilla stack:** plain HTML, CSS, and JavaScript — no frameworks, libraries, or build
  tools. The only external resource is the Lexend Google Font.
- **Inside the file:** inline `<style>` (CSS, theming, animations) near the top, the five
  step panels (`panel-0` … `panel-4`) plus modals in the HTML body, and an inline `<script>`
  (navigation, validation, drag-and-drop, progress tracking) near the bottom.
- **Client-side only:** there is no backend and no API calls. All progress is held in memory,
  so refreshing the page resets the walkthrough.
- **Desktop-oriented:** the layout assumes a wide screen and is not designed for mobile.

## Notes

- All content is demo/instructional data (for example, the sample contact "John Wick"); it is
  not connected to a live HubSpot instance.
- Progress is not saved between sessions — closing or refreshing the page starts over.
