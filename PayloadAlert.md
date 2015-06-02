# APNS Payload Custom Alert #

```

deviceToken = 'Qun\xaa\xd4R\x11zu\x07\x04\x9dG\xe6\x96j&\x95Y\x9d\x91~\xcc`z\n\x88O\xc0\x9c\xf6\xca' 

# create wrapper
wrapper = APNSNotificationWrapper('iphone_cert.pem', True)

# create message
message = APNSNotification()
message.token(deviceToken)

# create custom alert message
alert = APNSAlert()

# add body to alert
alert.body("Some alert message body")

# add localization key
alert.loc_key("ALERTMSG")

# add localization arguments
alert.loc_args(["arg1", "arg2"])

# add action button localization key
alert.action_loc_key("OPEN")

message.alert(alert)

# enable sound (default sound if no argument)
message.sound()

# add message to tuple and send it to APNS server
wrapper.append(message)
wrapper.notify()
```

# APNS Text Alert #

```

deviceToken = 'Qun\xaa\xd4R\x11zu\x07\x04\x9dG\xe6\x96j&\x95Y\x9d\x91~\xcc`z\n\x88O\xc0\x9c\xf6\xca' 

# create wrapper
wrapper = APNSNotificationWrapper('iphone_cert.pem', True)

# create message
message = APNSNotification()
message.token(deviceToken)

# just add alert text
message.alert("Very simple alert")

# enable sound (default sound if no argument)
message.sound()

# add message to tuple and send it to APNS server
wrapper.append(message)
wrapper.notify()
```
