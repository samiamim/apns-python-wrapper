# List of APNSWrapper exceptions #

### APNSTypeError ###
This exception raised when you try to add an argument with unexpected type.

### APNSPayloadLengthError ###
If length of payload more than 256 (by APNS specification) generate this exception

### APNSCertificateNotFoundError ###
This exception raised when you try to add an argument with certificate file but file not exist

### APNSValueError ###
This exception raised when you try to add value to method which expect concrete type of argument.

### APNSUndefinedDeviceToken ###
This exception raised when you try to send notifications by wrapper but one of notification don't have deviceToken.