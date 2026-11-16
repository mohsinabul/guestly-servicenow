# Three design decisions

## 1. Focus each role without relying on hidden buttons for security

Guests need their stay and requests. Front Desk needs booking and room information. A service agent needs their permitted team queue; a manager needs a wider operational view.

The later staff implementation uses role checks with `GlideRecordSecure` and record/field permission checks. Retained request-editor source also checks team visibility before loading a request, verifies write permission before saving, and compares `sys_mod_count` to detect stale edits.

These checks supplement the instance's ACLs. A role-specific screen is not evidence that another user's records cannot be reached. Current guest-isolation, cross-team access and direct-record denial tests still need to be run on the final instance.

## 2. Keep request context attached to the work

A booking connects a guest to their rooms. A guest request carries booking/room context and an assignment group, so the team can act on the correct room rather than relying on a message being passed along.

The earlier export contains the active `Guestly - Populate booking and room` Business Rule and `Intelligent Category Routing Flow`. The demo shows room-specific requests being handled by housekeeping. That supports the working path, but does not establish every invalid-booking or cross-guest submission case.

Internal notes and messages to the guest have separate inputs. This helps staff distinguish operational detail from a guest update; journal visibility still depends on the final ACLs and presentation rules.

## 3. Make chart selections and record lists agree

A dashboard should answer a question and let the manager inspect the records behind it.

The retained feedback implementation applies a shared date window and permission checks. Each chart honours the other selected filter: ratings follow the sentiment selection, sentiment counts follow the rating selection, and the table applies both. Average ratings use valid readable ratings from the matching records.

The dashboard reads stored sentiment instead of calling the analysis action whenever a chart is clicked. The first sentiment flow is inactive in the earlier export; V2 is active. Classifications assist review and should not be treated as infallible assessments of a guest's experience.

## Evidence boundary

These descriptions draw on retained development source, the supplied application export, screenshots and the approved demo. The retained source has not been freshly exported from the final instance, so it is implementation evidence rather than a guarantee that every current record is identical. See [configuration evidence](configuration-evidence.md) and [validation](validation.md).
