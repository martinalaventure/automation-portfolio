# Case Study — Smile Dental Clinic Assistant

## Problem

A dental clinic website needs to answer repetitive visitor questions and handle appointment requests efficiently.

Common requests include:
- asking for prices
- asking for opening hours
- requesting a consultation or appointment

Handling these interactions manually takes time and may delay responses.

## Solution

I built a lightweight assistant using Typebot and n8n.

### Front-end
Typebot provides a simple guided chat flow where users can:
- ask about prices
- ask about opening hours
- request an appointment

### Automation layer
n8n receives the user data through a webhook and routes the request.

Depending on the user's intent, the workflow:
- checks **Google Sheets** for clinic information such as services, prices, and hours
- uses **Gmail** to send an appointment request email to the clinic admin
- returns a final response back to Typebot

### Data source
Google Sheets acts as the source of truth for:
- clinic name
- opening hours
- services
- prices
- appointment policy

## Expected result

The expected result is a more efficient first-contact experience for the clinic:

- visitors get quick answers to common questions
- appointment requests are captured in a structured way
- the clinic admin receives clear email notifications
- repetitive manual work is reduced

## What this project demonstrates

This project demonstrates:
- end-to-end workflow automation
- no-code / low-code integration
- webhook-based communication
- structured service flows
- practical use of AI tools inside a business workflow

## Improvements for a next version

Future improvements could include:
- session-based memory
- multilingual support
- live appointment availability
- CRM integration
- better fallback handling for incomplete user input