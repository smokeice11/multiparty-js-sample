### Multi party Step 5: Inviting someone


>Warning: Do not forget to have your configuration (tokens, web hosting, etc.) set up as described [in the main MD fo the repository](https://github.com/sightcall/multiparty-js-sample/blob/master/readme.md). **Do not forget to modify the code to add your applicationId as well as your own URL to get a token.**  

#### Summary

In the step 5 the host can invite a attendee directly once the connference is hosted. No need to send the meeting point id. This is used to add someone on an already started conference.

####Implementation

#####On Host side

- Some html has been added to fill the uid of the user the host wants to invite. on the onclick() function, the command invite is sent.

- Addtional code used for notifying the host if the user accepted the invite is located in the OnConfCallHandler() function. It is associated with the action arguments ```joinRequestAccepted``` and ```joinRequestDenied```. Notification is added in the notification list.

#####On Attendee side

- Some code has been added to the OnConfCallHandler() function to notify the attendee that he has been invited. The associated action argument is ```attendeeInvited```.It triggers buttons to accept or refuse the invite.

