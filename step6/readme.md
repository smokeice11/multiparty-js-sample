### Multi party Step 6


>Warning: Do not forget to have your configuration (tokens, web hosting, etc.) set up as described [in the main MD fo the repository](https://github.com/sightcall/multiparty-js-sample/blob/master/readme.md). **Do not forget to modify the code to add your applicationId as well as your own URL to get a token.**  

#### Summary

In the step 6, an external user can join the multi party call. He connects as an external user of the user `host_uid`.

####Implementation

#####On Host side

- No change.  

#####On Attendee side

- The creation of the user has been changes on the new Rttc function. No more token is required and the associated code has been removed. Please note that you only have a limited number of external calls and this page could not authenticate if this number is exceeded.