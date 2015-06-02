# Aguments within Payload #

To add custom arguments to the Payload you should create instance or few instances of APNSProperty object. Arguments may be integer, string or array.

```

deviceToken = 'Qun\xaa\xd4R\x11zu\x07\x04\x9dG\xe6\x96j&\x95Y\x9d\x91~\xcc`z\n\x88O\xc0\x9c\xf6\xca' 

# create wrapper
wrapper = APNSNotificationWrapper('iphone_cert.pem', True)

# create message
message = APNSNotification()
message.token(deviceToken)
message.badge(5)

# here is argument *arg1* with integer value *54*
property1 = APNSProperty("arg1", 54)

# argument *arg2* with array of strings
property2 = APNSProperty("arg2", [ "val1", "val2" ])

# append properties to notification
message.appendProperty(property1)
message.appendProperty(property2)

# add message to tuple and send it to APNS server
wrapper.append(message)
wrapper.notify()
```