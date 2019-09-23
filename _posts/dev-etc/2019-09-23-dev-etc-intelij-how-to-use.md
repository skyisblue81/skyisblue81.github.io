---
layout: post
title: "[Tools] InteliJ 사용법"
subtitle: ""
categories: dev
tags: etc
---



> inflearn 강의 중 "IntelliJ를 시작하시는 분들을 위한 IntelliJ 가이드" 를 듣고  
> 그동안 IntelliJ를 사용하면서 조금더 잘 사용하기 위한것 들을 정리한 내용이다. 


<br><br>


jvm 메모리 설정
-----

`Help` - `Edit Custom VM Options...`

```
# custom IntelliJ IDEA VM options

-Xms1024m
-Xmx2048m
-XX:ReservedCodeCacheSize=240m
-XX:+UseCompressedOops
-Dfile.encoding=UTF-8
-XX:+UseConcMarkSweepGC
-XX:SoftRefLRUPolicyMSPerMB=50
-ea
-Dsun.io.useCanonCaches=false
-Djava.net.preferIPv4Stack=true
-Djdk.http.auth.tunneling.disabledSchemes=""
-XX:+HeapDumpOnOutOfMemoryError
-XX:-OmitStackTraceInFastThrow
-Xverify:none

-XX:ErrorFile=$USER_HOME/java_error_in_idea_%p.log
-XX:HeapDumpPath=$USER_HOME/java_error_in_idea.hprof
```

`-Xmx2048m` -> `-Xmx4096m` 으로 늘려준다.



<br><br>

---

<br><br>



단축키
-----

`control` + `shift` + `R` = main run

`command` + `d` = line copy
`command` + `delete` = line delete

`command` + `option` + `shift` + `<-` or `->` = element move (html)

`command` + `p` = 인자값 확인
![command + p]({{site.url}}/assets/img/post/dev-etc/2019-09-23-dev-etc-intelij-how-to-use/intelij-shortcut-command-p.png "command + p")

`option` + `space` = 코드구현부 확인
![option + space]({{site.url}}/assets/img/post/dev-etc/2019-09-23-dev-etc-intelij-how-to-use/intelij-shortcut-option-space.png "option + space")

`fn` + `F1` = 라이브러리 설명 확인
![fn + F1]({{site.url}}/assets/img/post/dev-etc/2019-09-23-dev-etc-intelij-how-to-use/intelij-shortcut-fn-f1.png "fn + F1")

`alt` + `<-` or `->` = 단어 이동

`shift` + `<-` or `->` = 드레그 이동

`fn` + `F2` = 에러코드로 이동

`command` + `E` = recent file list

`command` + `shift` + `A` = Action Search

`control` + `option` + `O` = 사용하지 않는 Import 정리



<br><br>

---

<br><br>



Auto Import
-----

`Editor` - `General` - `Auto Import`
![Auto Import]({{site.url}}/assets/img/post/dev-etc/2019-09-23-dev-etc-intelij-how-to-use/intelij-auto-import.png "Auto Import")



<br><br>

---

<br><br>



Live Template (code template)
-----

psvm : public static void main
psf : public static final
sout : System.out.println()

command + j = Live Template List

* Live Templat 추가하기

![Live Templat Step 1]({{site.url}}/assets/img/post/dev-etc/2019-09-23-dev-etc-intelij-how-to-use/intelij-live-templat-step-1.png "Live Templat Step 1")
![Live Templat Step 2]({{site.url}}/assets/img/post/dev-etc/2019-09-23-dev-etc-intelij-how-to-use/intelij-live-templat-step-2.png "Live Templat Step 2")
![Live Templat Step 3]({{site.url}}/assets/img/post/dev-etc/2019-09-23-dev-etc-intelij-how-to-use/intelij-live-templat-step-3.png "Live Templat Step 3")
![Live Templat Step 4]({{site.url}}/assets/img/post/dev-etc/2019-09-23-dev-etc-intelij-how-to-use/intelij-live-templat-step-4.png "Live Templat Step 4")



<br><br>

---

<br><br>



디버깅
-----

![debug]({{site.url}}/assets/img/post/dev-etc/2019-09-23-dev-etc-intelij-how-to-use/intelij-debug-add-option.png "debug")

숫자면 i==5
문자면 i.equals(“5")

⌘