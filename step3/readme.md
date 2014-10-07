### Multi party Step 3: Managing the Joining Request in default mode


>Warning: Do not forget to have your configuration (tokens, web hosting, etc.) set up as described [in the main MD fo the repository](https://github.com/sightcall/multiparty-js-sample/blob/master/readme.md). **Do not forget to modify the code to add your applicationId as well as your own URL to get a token.**  

#### Summary

In the step 3 the meeting Point is in default mode. The host has to accept any attendee requesting to enter the conference.

####Implementation

#####On Host side

- The javascript code used for joining request is located in the OnConfCallHandler() function. It is associated with the action ```joinRequest```. For each request a button is added to accept or refuse the attendee in the request list part of the html.

- Some html code has been added to show the notifications (div id request)


#####On Attendee side

- Some code has been added to the OnConfCallHandler() function to notify the attendee of his request status. The associated actions arguments are ```attendeePending```, ```attendeeAccepted``` or ```attendeeDenied```.

