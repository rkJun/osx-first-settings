# OS X First Settings of My Style

어느 웹 개발자의 개인 스타일 맞춤형 OS X 개발환경 세팅. **ver. rkJun**

[펭귄너구리](http://blog.doortts.com)님의 글[^1]을 보고, 저도 개인적인 정리 차원에서 올려둡니다.

[^1]: 펭귄너구리님의 어떤 개발자의 맥환경 <https://github.com/doortts/env-of-mac>

## 시스템환경설정

- 핫코너
- 키보드
- iCloud 설정 등
 
## AppStore
- Update
- *iPhoto, iMovie*
- *Xcode*
  - *Command Line Tools* (Xcode - Preferences - Downloads)

## 구름입력기 설치
세벌식 사용자 또는 vi 사용자에게 유리

- esc 키 로마자전환 활성

***
## Homebrew 설치

$```ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"```

$```brew doctor```

### Homebrew 로 설치하기

#### git
$```brew install git```

#### node
$```brew install node```
***
## dotfiles 적용
.files, including ~/.osx — sensible hacker defaults for OS X

<https://github.com/mathiasbynens/dotfiles>

기본적으론 dotfiles 를 사용하고,
**.extra** 에 확장 또는 덮어쓸 명령을 추가한다.

My Extra Style :  
<https://github.com/rkJun/dotfiles/blob/master/.extra>



***
## Homebrew-cask 설치

a friendly homebrew-style CLI workflow for the administration of Mac applications distributed as binaries

<https://github.com/phinze/homebrew-cask>

### Homebrew cask 로 application 설치

#### 구글크롬
$```brew cask install google-chrome``` 

#### iterm2
$```brew cask install iterm2```

#### Sublime Text 
$```brew cask install sublime-text```

#### 그외 
$```brew cask install google-chrome-canary```

$```brew cask install macvim```

$```brew cask install transmission```

$```brew cask install mplayerx```

$```brew cask install vlc```

$```brew cask install virtualbox```

$```brew cask install dropbox```

$```brew cask install caffeine```

$```brew cask install alfred```

$```brew cask install mou```

---
## JDK 설치

### JDK6 설치

$```java``` 또는 $```javac```

### JDK7 설치

Oracle 사이트에서 다운로드  
<http://www.oracle.com/technetwork/java/javase/downloads/index.html>

 oracle JDK7 설치경로 :  
 _/Library/Java/JavaVirtualMachines/jdk1.7.0_25.jdk/Contents/Home_


===
## 유용한 팁
1. 모두 표시 (CMD+OPT+SHIFT+H) 단축키 추가 및 Dock Icon (숨김시) 투명 적용  
   <http://macnews.tistory.com/1054>
   ![macnews icon](http://cfile27.uf.tistory.com/original/206B013E4FE755FD15303C "macnews.tistory.com")
   
   $```defaults write com.apple.Dock showhidden -bool YES && killall Dock```

2. 웹브라우저용 스타일 시트 적용  
   <http://macnews.tistory.com/162> ![macnews icon][mnfavi]

[mnfavi]: http://cfile27.uf.tistory.com/original/206B013E4FE755FD15303C "macnews.tistory.com"
   

## Java IDE 설치

* Spring Tool Suite <http://www.springsource.org/sts>  

또는
 
* Eclipse IDE for Java EE Developers <http://www.eclipse.org/downloads/>

## git 최신 사용

Xcode (Command Line Tools) 내장 git 이 아닌, brew install 한 git 을 사용하도록, /usr/local/bin 을 $PATH 보다 먼저 잡는다.

```
# path override setting for new git
export PATH="/usr/local/bin:$PATH"
```

## 가상머신 설치
* VMWare Fusion
* Parallels 
* VirtualBox

Vmware Fusion 삭제 관련 링크 :  
<http://kb.vmware.com/selfservice/microsites/search.do?cmd=displayKC&docType=kc&docTypeID=DT_KB_1_1&externalId=1017838>

### Sublime Text 설정

[Sublime Text][st] 설정하기


[st]: http://sublimetext.com

### NTFS 외장하드 사용하기

[OS X 에서 NTFS 쓰기. FUSE for OS X, 그리고 NTFS-3G](http://rkjun.wordpress.com/2013/07/14/os-x-%EC%97%90%EC%84%9C-ntfs-%EC%93%B0%EA%B8%B0-fuse-for-os-x-%EA%B7%B8%EB%A6%AC%EA%B3%A0-ntfs-3g/)

### 추가폰트 적용
서체관리자 실행후 폰트 파일 복사

* 나눔고딕코딩  
   <http://dev.naver.com/projects/nanumfont>

 
<!--
> Right angle brackets &gt; are used for block quotes.
> 
~~Strikethrough~~

```
Fenced code blocks are like Stardard Markdown’s regular code
blocks, except that they’re not indented and instead rely on
a start and end fence lines to delimit the code block.
```

First Header | Second Header | Third Header
------------ | ------------- | ------------
Content Cell | Content Cell  | Content Cell
Content Cell | Content Cell  | Content Cell

If you wish, you can add a leading and tailing pipe to each line of the table:

| First Header | Second Header | Third Header |
| ------------ | ------------- | ------------ |
| Content Cell | Content Cell  | Content Cell |
| Content Cell | Content Cell  | Content Cell |

Specify alignement for each column by adding colons to separator lines:

First Header | Second Header | Third Header
:----------- | :-----------: | -----------:
Left         | Center        | Right
Left         | Center        | Right
-->

<!--### Shortcuts

#### View

* Toggle live preview: Shift + Cmd + I
* Toggle Words Counter: Shift + Cmd + W
* Toggle Transparent: Shift + Cmd + T
* Toggle Floating: Shift + Cmd + F
* Left/Right = 1/1: Cmd + 0
* Left/Right = 3/1: Cmd + +
* Left/Right = 1/3: Cmd + -

#### Actions

* Copy HTML: Option + Cmd + C
* Strong: Select text, Cmd + B
* Emphasize: Select text, Cmd + I
* Inline Code: Select text, Cmd + K
* Strikethrough: Select text, Cmd + U
* Link: Select text, Control + Shift + L
* Image: Select text, Control + Shift + I
* Select Word: Control + Option + W
* Select Line: Shift + Cmd + L
* Select All: Cmd + A
* Deselect All: Cmd + D
* Convert to Uppercase: Select text, Control + U
* Convert to Lowercase: Select text, Control + Shift + U
* Convert to Titlecase: Select text, Control + Option + U
* Convert to List: Select lines, Control + L
* Convert to Blockquote: Select lines, Control + Q
* Convert to H1: Cmd + 1
* Convert to H2: Cmd + 2
* Convert to H3: Cmd + 3
* Convert to H4: Cmd + 4
* Convert to H5: Cmd + 5
* Convert to H6: Cmd + 6
* Convert Spaces to Tabs: Control + [
* Convert Tabs to Spaces: Control + ]
* Insert Current Date: Control + Shift + 1
* Insert Current Time: Control + Shift + 2
* Insert entity <: Control + Shift + ,
* Insert entity >: Control + Shift + .
* Insert entity &: Control + Shift + 7
* Insert entity Space: Control + Shift + Space
* Insert Scriptogr.am Header: Control + Shift + G
* Shift Line Left: Select lines, Cmd + [
* Shift Line Right: Select lines, Cmd + ]
* New Line: Cmd + Return
* Comment: Cmd + /
* Hard Linebreak: Control + Return

 
#### Export

* Export HTML: Option + Cmd + E
* Export PDF:  Option + Cmd + P

 
For feedback, use the menu `Help` - `Send Feedback`-->