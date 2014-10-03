### Multi Pary Examples
Here you will find example source code for implementing multy party calls.

We have broken up in 7 examples described below, for implementation details click on the link after each section


step 1:
the host.html file can create a meeting point. Once hosted, an attendee can join the conference by navigating to attende1.html and clicking "join"

Step 2:
Same configuration as step 1, with added notification before meeting point is hosted; when an attendee navigates to the attendee page and joins the conference, a notification will be sent to the host.html page
Step 3:
Same configuration as step 2 but we turn off auto-accept; now the host will be asked if he wants to allow the user that navigates to the attendee.html page and click join the attendee page now shows wether their request to attend is pending, accepted or denied.
Step 4 :
Same configuration as step 3 be we add buttons to allow the host to controll the mode; he can now set it to:
 - "default" -  once the host clicks "host", he will be asked to "accept" or "deny" each attendee
 - "auto-accept" - once the host clicks "host", all attendees are automcatically accepted into the conference.
 - "locked" - attendees will automatically recieved a  "denied" answer when trying to "join"
Step 5:
 Same configurations as step 4 but the host can now invite an attendee once the conference has started. The attendee can  "accept" or "deny" the invite.
Step 6:
External.html: new page identical to step3 attendee but external user.