# Make.com Lead Intake & Routing Automation

## Overview
An automated lead intake pipeline built in Make.com. The workflow captures webform submissions in real time via Custom Webhooks, checks incoming records against existing data to prevent duplicate triggers, standardizes payload fields, and sends structured notification emails to account managers.

## System Architecture
1. **Custom Webhook:** Real-time ingestion of lead submission payloads (`name`, `email`, `budget`, `message`).
2. **Deduplication Check:** Queries existing records to verify if the email address has already been processed, preventing redundant tasks.
3. **Gmail Integration:** Merges webhook fields into a structured HTML/text template delivered directly to the sales team.

## Repository Contents
- `blueprints/lead_routing_scenario.json` - Complete scenario export for Make.com.
- `screenshots/` - Workflow layout and canvas visual references.

## How to Import & Use
1. Download `blueprints/lead_routing_scenario.json` from this repository.
2. Log into **Make.com** and create a new Scenario.
3. Click the **three dots (...)** menu in the bottom control bar and select **Import Blueprint**.
4. Upload the JSON file.
5. Re-bind your Webhook listener and Gmail connections in the imported modules.
