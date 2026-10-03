# Dagplanning instructions

When the user provides a day plan, update `Dagplanning.ics` directly in this repository.

- Preserve existing appointments unless the user explicitly changes or removes them. Add new appointments without replacing unrelated entries.
- Give each appointment a stable iCalendar `UID` derived deterministically from its title, date, and start time. Use the same normalization and namespace consistently so an unchanged appointment keeps the same UID on later edits. If an appointment's title, date, or start time changes, its UID changes accordingly.
- Keep the ICS file valid and retain existing appointment details that the user has not asked to change.
- After updating the calendar, commit the change and push it to `origin/main`.
- Do not invoke a GitHub Actions workflow to generate or update the calendar; it has been removed.
