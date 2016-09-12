---
title: "Homebrew Update Bug 해결방법"
categories: [system, macOS]
tags: [bugs]
keywords: homebrew, bug
summary: "macOS Homebrew Update시 항상 up-to-date라고 나오는 버그를 해결하는 방법을 설명합니다."
permalink: homebrew_update_bug.html
thumb: software-bug.jpg
---
맥용 패키지 관리자인 Homebrew에 버그가 발생했습니다.
만약 2016년 8월 10일 ~ 11일 사이에 Homebrew를 업데이트 했다면(brew update) 그 이후에 brew update시 항상 up-to-date라고 나오는 버그입니다.

해결방법은 간단한데요, 터미널 창에서 아래와 같이 입력하시면 됩니다.

```bash
cd $(brew --repo); git fetch; git reset --hard origin/master
```

이후 다시 업데이트를 하면 잘 되는 것을 확인할 수 있습니다.

```bash
brew update
```

그 수 많은 패키지들이 며칠동안 업데이트가 없길래 혹시나 Homebrew 문 닫은 줄 알고 걱정했었는데, 다행히 별 문제는 없나 봅니다.  
<img src="http://emojipedia-us.s3.amazonaws.com/cache/28/10/281085c6e7d7d6059b8586abcb084621.png" width="28px">

- - -

**참조**

* [Homebrew](http://brew.sh)
* [GitHub Link](http://stackoverflow.com/questions/38945084/homebrew-mac-update-issues)
 

**관련글**

* [Homebrew 설치하기](homebrew.html)