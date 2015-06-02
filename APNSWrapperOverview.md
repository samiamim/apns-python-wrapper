# Apple Push Notification Python Wrapper #

## Introduction ##
Apple Push Notification Wrapper is very simple tool to sending your notification to your apps on iPhone / iPod Touch devices. This document doesn't describe how to generate APNS certificate.

## Installation ##
To install APNSWrapper use setuptools. Type in your terminal:
```
$ easy_install APNSWrapper
```

## Basic Usage ##

To send your notification you should make few things:
  * create APNSNotificatonWrapper (in sandbox or production mode)
  * create an instance or few instances of APNSNotification
  * set your notification type (badge, sound or alert)
  * send notification

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