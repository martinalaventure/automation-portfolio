# Smile Dental Clinic Assistant

A lightweight clinic assistant built with **Typebot + n8n + Google Sheets + Gmail**.

## What it does

This project helps a dental clinic handle common website interactions:

- answers questions about **prices**
- answers questions about **opening hours**
- collects **appointment requests**
- sends an email notification to the clinic admin when a user wants to book an appointment

## Tech stack

- **Typebot** for the front-end chat flow
- **n8n** for workflow orchestration
- **Google Sheets** as the clinic knowledge base
- **Gmail** to notify the admin
- **LLM model** connected through the n8n AI Agent

## Main flow

1. The visitor selects an option in Typebot
2. Typebot collects the necessary information
3. Typebot sends the data to an n8n webhook
4. n8n decides what to do:
   - if it is a pricing or opening-hours question, it checks Google Sheets
   - if it is an appointment request, it sends an email to the admin
5. n8n returns a final reply to Typebot
6. Typebot displays the reply to the user

## Example use cases

- “How much is whitening?”
- “Are you open on Saturday?”
- “I want to book an appointment for teeth whitening Tuesday 5th April at afternoon.”

## Repository contents

- `workflow/` → exported n8n workflow JSON
- `assets/` → screenshots of the implementation
- `case-study.md` → short project case study

## Notes

- Credentials and sensitive data should not be committed.
- Google Sheets acts as the source of truth for services, prices, and opening hours.
- Gmail is used only for appointment notifications.

## Project goal

This project was built as a portfolio piece to demonstrate:
- workflow automation
- AI-assisted service routing
- integration between no-code tools and external services
- practical business automation design