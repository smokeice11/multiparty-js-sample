### Multi Party Examples

Here you will find example source code for implementing multy party calls. At any time do not hesitate to refer to our [API Reference](http://docs.sightcall.com/GD/01_javascript/10_api_js_internal/) or to the multi party [How-To](http://docs.sightcall.com/GD/01_javascript/05_js_multiparty.html). If needed, definitions are available [here](http://docs.sightcall.com/GD/06_definitions.html)


#### Requirements

>It is strongly recommended to have already set up and run the 1 to 1 example available [here on GitHub](https://github.com/sightcall/one-to-one-js-sample)  

The requirements are the same as for the 1 to 1 Sample:  

- It is important that the project is served from a webserver and not from the file system when using WebRTC.
- Be aware of your AppId, and understand what is a ```UID``` and a ```Display Name```. All of them are described in our [definition page](https://docs.sightcall.com/GD/06_definitions.html).

You can find more details about AppID, UID and Display Name [here](https://docs.sightcall.com/GD/01_javascript/01_jsquickstart.html)

You also need to be able to get tokens out of the weemo cloud. The fastest way to obtain a token is to use one of our Authentication Client for backends. Description and samples are available [here](https://docs.sightcall.com/GD/04_backend/).

##### Setting up the AppID and the Authentication URL

Once you have received your ```AppID``` provided by Sightcall, you can setup these examples with your AppId in order to test the API. The only thing you have to do is to setup the ```AppId``` as well as the Authentication URL.
To do so, for each of the Javascript examples you want to use, you must edit the .html file and
replace the placeholder "YOUR_APP_IDENTIFIER" by your AppID in the following lines"

```html
<script type="text/javascript" src="https://download.rtccloud.net/js/webappid/YOUR_APP_IDENTIFIER"></script>
```

and 

```JavaScript
var rtcc = new Rtcc("YOUR_APP_IDENTIFIER", "callee_uid", "internal", options);
```

You also need to replace the following line if you are using our java, node.js or ruby Authentication API Client sample:

```
//AUTH_URL = 'http://YOUR_AUTH_URL/gettoken?uid=',
```
 or if you are using our PHP Authentication API Client Sample.

```
// AUTH_URL = 'http://YOUR_AUTH_URL/gettoken.php?uid=',

```
In any case, you have to uncomment the right line and specify the URL where a token can be found by the web page.
Of course, if you have implemented your own client parameters and URL might be different and you need to update the samples accordingly.

Now you can upload the examples on a webserver and start using them.


#### Use Examples

We have broken up in six examples described below, for implementation details click on the link after each section


step 1:
See how the Host(host.html) creates a meeting point and then hosts it. Once hosted, an attendee(attende1.html) can join the conference by filling the Meeting Point field with the value shown on the host page and clicking "join".  
Please note that the conference is set up in auto-accept mode so that any user having the Meeting Point Id can enter the conference.  
If you wish to have more than one attendee, just create another page attendee2.html and replace the 
```var UID_USER = 'attendee1_uid'``` by a new uid like ```var UID_USER = 'attendee2_uid'```.
For more clarity you should replace also ```displayName : 'Attendee1',``` by ```displayName : 'Attendee2',```

Step 2:
See how the Host is notified before hosting the Meeting Point that some users are waiting his arrival to enter the conference.
The configuration is the same as step 1 but notification before hosting are handled in the host.html file.  

Step 3:
See how to accept or deny users entring the conference and how users are notified of their status.  
The configuration is the same as step 2 but we have turned off auto-accept; now the host is asked to allow the user that navigates to the attendee1.html page and click join. The attendee page now shows wether their request to attend is pending, accepted or denied.  

Step 4 :
See how to change the mode of the Meeting Point.  
The configuration is the same as step 3 be we have added buttons to allow the host to controll the mode; he can now set it to:
 - "default" -  once the host clicks "host", he will be asked to "accept" or "deny" each attendee
 - "auto-accept" - once the host clicks "host", all attendees are automatically accepted into the conference.
 - "locked" - attendees will automatically recieved a  "denied" answer when trying to "join"  

Step 5:
See how to invite someone "on the fly" into a conference. The user does not need to have received the Meeting Point Id.
The configuration is the same as step 4 but the host can now invite an attendee once the conference has started. The attendee can  "accept" or "deny" the invite.  

Step 6:
See how to connect to a conference as an external attendee.
External.html: new page identical to step3 attendee but connecting as an external user.