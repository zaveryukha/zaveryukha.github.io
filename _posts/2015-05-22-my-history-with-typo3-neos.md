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