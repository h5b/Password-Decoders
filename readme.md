Some simple password decoders that I've hacked together whilst onsite.

decodejenkins.py
================
This will decode credential hashes found in Jenkins config and credentials.xml files. I wrote this as https://github.com/tweksteen/jenkins-decrypt failed to work on the version of Jenkins I was looking at - it appears that some structure changes were put in place in the later versions.

To work it needs the master.key and hudson.util.Secret file from the Jenkins root directory. These are generated per host.

The hash can be identified as it should be surrounded by braces, be base64 encoded and start with "AQAAABAAAAAQ"