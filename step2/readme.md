### Multi party Step 2


>Warning: Do not forget to have your configuration (tokens, web hosting, etc.) set up as described [in the main MD fo the repository](https://github.com/sightcall/multiparty-js-sample/blob/master/readme.md). **Do not forget to modify the code to add your applicationId as well as your own URL to get a token.**  

#### Summary

In the step 2 the host is notified for each user trying to enter the conference before the conference is hosted.

####Implementation

#####On Host side

- The javascript code used for notification of the host is located in the OnConfCallHandler() function. It is associated with the action ```joinRequestNotification```.

- Some html code has been added to show the notifications (div notifications)


#####On Attendee side

- No difference with Step 1
