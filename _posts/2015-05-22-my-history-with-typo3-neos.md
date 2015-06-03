---
layout: post
title: My history with TYPO3 Neos
date: 2015-05-25 14:50:00
tags: neos
comments: true
published: true
---

## Day 1

### Read right documentation topic

Issue: After adding package to project web container failed to start

First of all you should read right documentation topic (smile)
[link](http://docs.typo3.org/flow/TYPO3FlowDocumentation/TheDefinitiveGuide/PartII/Kickstart.html)

For creating a package I used the command
```./flow package:create```

Solution:
```./flow kickstart:package```
But this doesn't solve issue with starting of the web container.
I had to remove docker containers:
`docker-compose rm -v`

## Day 2

### Google it!

Issue: access to container by ssh not working.

{% highlight bash %}
localhost:neos john_doe$ ssh -p1122 www@192.168.59.103
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@    WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED!     @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
IT IS POSSIBLE THAT SOMEONE IS DOING SOMETHING NASTY!
Someone could be eavesdropping on you right now (man-in-the-middle attack)!
It is also possible that a host key has just been changed.
The fingerprint for the RSA key sent by the remote host is
**:**:**:**:**:**:**:**:**:**:**:**:**:**:**:**.
Please contact your system administrator.
Add correct host key in /Users/john_doe/.ssh/known_hosts to get rid of this message.
Offending RSA key in /Users/john_doe/.ssh/known_hosts:6
RSA host key for [192.168.59.103]:1122 has changed and you have requested strict checking.
Host key verification failed.
{% endhighlight %}

Solution:
```
localhost:neos john_doe$ cd ~
localhost:~ john_doe$ rm .ssh/known_hosts
```