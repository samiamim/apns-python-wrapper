<img src='http://apns-python-wrapper.googlecode.com/files/apple-push-notification-service-python-2.png' align='left' width='250' alt='Apple Push Notification Python Wrapper' height='214' /><br /><br /><br />This is Python wrapper for **[Apple Push Notification Service](http://en.wikipedia.org/wiki/Apple_Push_Notification_Service)**.
<br /><br />
The Wrapper support for alerts, badges, sounds and custom arguments. **[Package on Python Package Index](http://pypi.python.org/pypi/APNSWrapper/)**
<br />
There is NO DEPENDENCY to **ssl** python module. This library have build-in support for **openssl command-line tool** (openssl s\_client)
<br /><br />

**This project looking for a sponsor: I need an iPhone (I don't care about model - the only requirement is to support latest iOs) and access to iPhone developer center to test the service**. Please contact klymyshyn at gmail com if you can help me with this project.

<br /><br /><br />
## News ##
  * **May 19, 2010:** New version of APNSWrapper 0.6.1. Fixed [Issue #6](https://code.google.com/p/apns-python-wrapper/issues/detail?id=#6) - everyone upgrade from 0.5 to 0.6.1 as soon as possible - in 0.5 release was ssl module reference issue ([changelog](http://apns-python-wrapper.googlecode.com/hg/CHANGELOG))
  * **April 24, 2010:** New version of APNSWrapper 0.5. Fixed known issues ([Issue #3](https://code.google.com/p/apns-python-wrapper/issues/detail?id=#3) and [Issue #5](https://code.google.com/p/apns-python-wrapper/issues/detail?id=#5)), added checking of unicode strings and some small improvements of code ([changelog](http://apns-python-wrapper.googlecode.com/hg/CHANGELOG))
  * **April 24, 2010:** New version of APNSWrapper 0.5. Fixed known issues ([Issue #3](https://code.google.com/p/apns-python-wrapper/issues/detail?id=#3) and [Issue #5](https://code.google.com/p/apns-python-wrapper/issues/detail?id=#5)), added checking of unicode strings and some small improvements of code ([changelog](http://apns-python-wrapper.googlecode.com/hg/CHANGELOG))
  * **November 17, 2009:** New version of APNSWrapper 0.4. There is couple of new features - removed dependency form SSL module, improved code and added patch by eric.chamberlain. Also I've tested it (at last) in real-world and it works perfectly.  One last thing – the Feedback service haven't tested yet (I can't reproduce it :( ). My appreciation for people who interested in this project and spent time to support of APNSWrapper:
    * eric.chamberlain
    * Casey E
    * Henry Grant
    * Michael Hanna
and others.
Thank you!

  * **August 11, 2009:** APNSWrapper source code is available. Also have fixed bug with wrong production URL for APNSNotification class

## Docs ##
  * [APNSWrapper overview](APNSWrapperOverview.md)
  * [Custom Payload alert](PayloadAlert.md)
  * [Using Feedback Service](FeedbackService.md)
  * [Custom Payload arguments](customArguments.md)
  * [Exceptions](Exceptions.md)

## Known Issues ##
  * [SSL module installation issue](SSLInstallationIssue.md)


## Simple How-To ##
```

deviceToken = 'Qun\xaa\xd4R\x11zu\x07\x04\x9dG\xe6\x96j&\x95Y\x9d\x91~\xcc`z\n\x88O\xc0\x9c\xf6\xca' 

# create wrapper
wrapper = APNSNotificationWrapper('iphone_cert.pem', True)

# create message
message = APNSNotification()
message.token(deviceToken)
message.badge(5)

# add message to tuple and send it to APNS server
wrapper.append(message)
wrapper.notify()
```


## Support ##
Contact klymyshyn at gmail com for support