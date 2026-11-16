# Configuration evidence

The owner supplied an earlier application update set and confirmed that the later staff portal was developed separately on a PDI and then moved to the working instance. The two supplied update-set XML files are byte-for-byte identical. They were reviewed locally and are not included in this public showcase package.

## Active configuration in the earlier export

| Type | Verified names |
| --- | --- |
| Flows | Booking - Check-in Room; Booking - Check-out Room; Intelligent Category Routing Flow; Resolution Timestamp Auto-Stamping; Guestly Feedback Sentiment Analysis V2 |
| Business Rules | Validate Booking Dates; Force pending on Missing Info; Guestly - Populate booking and room |
| Client Script | Show Only Most Recent Work Note |
| UI Policies | Require actual check-out date; Require cleanliness state; Require completion date when closed; Require assignee when group is selected; Require room allocation when checked in; Require actual check-in date; Lock status when room is out of order |
| Notifications | Request Work in Progress; Request Closed Incomplete; Request Confirmation; Checkout & Digital Receipt Email; Request Pending Information Alert; Pre-arrival Welcome; Request Closed Complete; Reservation Confirmation; Booking Confirmation |

The earlier export also contains inactive configuration: Guestly - Housekeeping Fulfilment, the first Guestly Feedback Sentiment Analysis flow, and Lock Guest Request for guests. These are not presented as active features. Housekeeping fulfilment in the showcase refers to the demonstrated staff workflow.

The exported Guestly Weather and Explore Nearby widgets contain Open-Meteo / RESTMessageV2 integration code. Explore Nearby also contains a map iframe and Google Maps links. This supports an embedded-map description, not a claim that a custom Google Maps API integration was built.

## Later staff portal evidence

The supplied screenshots and recorded walkthrough show the Front Desk, housekeeping and manager views, including room-specific booking information, request assignment and editing, separate internal/guest message inputs, operational charts, feedback ratings and stored sentiment. Earlier staff-widget source supplied during development supports the implementation description of client controllers and server-side access checks.

## Limits

An active flag in an export confirms configuration state at export time, not successful execution today. Screenshots do not establish email delivery, permission enforcement or sentiment accuracy. The full current AI configuration and every cross-scope dependency have not been re-exported. No custom language model or production performance result is claimed.
