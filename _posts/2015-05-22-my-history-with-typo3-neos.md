---
layout: post
title: My history with TYPO3 Neos
date: 2015-05-25 14:50:00
tags: neos
comments: true
published: true
---

## Day 1

### Read rigt documentation topic

Первым делом надо прочитать правильную документацию (улыбка)
[ссылка](http://docs.typo3.org/flow/TYPO3FlowDocumentation/TheDefinitiveGuide/PartII/Kickstart.html)

Оказывается packege нужно было делать не командой 
`./flow package:create`
а командой 
`./flow kickstart:package`
В итоге пришлось удалить контейнеры docker'а:
`docker-compose rm -v`

## Day 2

### Google it!

При попытке войти по ssh вылезла ошибка
```
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
```

Решение
```
localhost:neos john_doe$ cd ~
localhost:~ john_doe$ rm .ssh/known_hosts
```

При следующем заходе система попросит подтвердить вход.