# Dental Clinic App — User Funnel Analysis

A beginner product analytics project focused on analyzing user behavior in a simulated dental clinic app using Python, SQLite, and SQL.

## Project Overview

The project uses synthetic data to simulate users, sessions, and events in a dental clinic application. The goal is to explore how users move through the app and identify conversion between key stages of the appointment-booking funnel.

All data in this project is synthetic and generated for educational purposes.

## Dataset

The database contains three tables:

* `users` — user IDs, devices, acquisition sources, and registration dates.
* `sessions` — session IDs, user IDs, and session start times.
* `events` — event IDs, user IDs, session IDs, event names, and event timestamps.

The dataset simulates 3,000 users.

## User Funnel

The simulated user journey includes the following events:

1. `app_open` — opens the app.
2. `view_services` — views available services.
3. `view_service_details` — views details about a service.
4. `view_doctor` — views a doctor’s profile.
5. `select_time` — selects an appointment time.
6. `book_appointment` — books an appointment.

## Tools

* Python — synthetic data generation
* Pandas and NumPy — data generation and initial exploration
* SQLite — database storage
* SQL — event analysis, unique-user counts, and data quality checks

## Initial Results

| Funnel Event                 | Unique Users |
| ---------------------------- | -----------: |
| App opened                   |        3,000 |
| Viewed services              |        2,795 |
| Viewed service details       |        2,380 |
| Viewed a doctor              |        1,780 |
| Selected an appointment time |        1,047 |
| Booked an appointment        |          776 |

The ratio of users who booked an appointment to users who opened the app is approximately **25.9%**.

This is an initial event-based conversion measure. A more rigorous funnel analysis should explicitly define the required event sequence and the unit of analysis, such as users or sessions.

## SQL Analysis

The project includes queries to:

* Count distinct users for each event
* Summarize event counts in funnel order
* Check for duplicate events
* Compare timestamps of funnel events using a common table expression (CTE)

## How to Run

The data-generation script was initially designed for Google Colab and uses `google.colab.files` to download the generated SQLite database.

To run it outside Google Colab, remove or adapt the Colab-specific download code and execute the Python script in an environment with the required libraries installed.

The generated database contains the `users`, `sessions`, and `events` tables for further SQL analysis.

## Project Status

In progress.

Planned improvements:

* Calculate conversion rates between consecutive funnel stages
* Analyze time between funnel events
* Compare user behavior by device and acquisition source
* Simulate an A/B test and evaluate the results

## Use of AI

AI tools were used to assist with parts of the Python data-generation script. SQL queries and the initial analysis were written independently.
