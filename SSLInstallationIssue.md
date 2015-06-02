# The Problem #
If you don't have **ssl** module into your environment (Python 2.5) than probably you not be able to install APNSWrapper via **easy\_install**.

# The Solution #
The solution is download and install **ssl** module by hand. You should make following:
  1. download **ssl** .tar.gz file from **[ssl module page on PyPI](http://pypi.python.org/pypi/ssl/)**
  1. unarchive and run
```
$ tar -xzf ssl-1.14.tar.gz && python setup.py build && python setup.py install
```
  1. check the installation:
```
% python
Python 2.5.2 (r252:60911, May 24 2008, 20:08:55) 
[GCC 3.4.6] on sunos5
Type "help", "copyright", "credits" or "license" for more information.
>>> import ssl
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
  File "ssl/__init__.py", line 60, in <module>
    import _ssl2             # if we can't import it, let the error propagate
ImportError: No module named _ssl2
```

If you get ImportError exception you should do something like in [this article](http://www.upfrontsystems.co.za/Members/hedley/my-random-musings/python-ssl-no-module-named-_ssl2) - Go to ${PYTHON\_HOME}/lib/python2.4/site-packages/ssl and delete the init.pyc file.

The **ssl** module should work.

# Next step #
Installation of APNSWrapper via easy\_install should be complete.
```
$ easy_install APNSWrapper
```