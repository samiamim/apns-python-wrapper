# Feedback Service #

Periodically you may get list of devices where your app is uninstalled. For this purpose you should use Feedback Service. APNSFeedbackWrapper object always return tuple with two values – time and deviceToken. Time in datetime.datetime format.

```
feedback = APNSFeedbackWrapper('iphone_cert.pem', True)
feedback.receive()
	
print "\n".join("%s at %s" % (str(y), x.strftime("%m %d %Y %H:%M:%S")) for x, y in feedback])

```