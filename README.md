# OS X First Settings of My Style

어느 웹 개발자의 개인 스타일 맞춤형 OS X 개발환경 세팅.  
**```OS X 10.9 Mavericks``` 를 기준으로 작성했습니다.**

[펭귄너구리](http://blog.doortts.com)님의 글(어떤 개발자의 맥환경 <https://github.com/doortts/env-of-mac>)
을 보고, 저도 개인적인 정리 차원에서 올려둡니다.


## 시스템환경설정

- 핫코너
  - 좌상 - Mission Control
  - 우상 - 알림센터
  - 좌하 - 응용프로그램 윈도우
  - 우하 - Dashboard
- 키보드
  - 키반복 최대한 빠르게, 반복지연시간 최대한 짧게
  - 모든 F1, F2 등의 키를 표준 기능 키로 사용 체크
  - 조합키 - Caps Lock 키를 ^Control 키로 변경
  - 단축키탭 - 전체 키보드 접근 - 모든 컨트롤 선택
- iCloud 설정 등
 
## AppStore
- Update
- *iPhoto, iMovie*
- *twitter*
- *Xcode*
  - *Command Line Tools*
  ```SHELL
  $ xcode-select --install
  ```

## 구름입력기 설치
<http://gureum.org/> 세벌식 사용자 또는 vi 사용자에게 유리  
- esc 키 로마자전환 활성

***
## Homebrew 설치

```SHELL
$ ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"
... ...
$ brew doctor

``` 
From [Homebrew 공식사이트 한글](http://brew.sh/index_ko.html)

### Homebrew 로 설치하기

#### git, zsh, tmux
```SHELL
$ brew install git
$ brew install zsh
$ brew install tmux
```
##### oh-my-zsh
```SHELL
$ curl -L http://install.ohmyz.sh | sh
```

#### node
```SHELL
$ brew install node
```

#### tig
Text-mode interface for git
```SHELL
$ brew install tig
```

#### jq 
command-line JSON processor
```SHELL
$ brew install mongodb
```

#### peco
Simplistic interactive filtering tool
```SHELL
$ brew install peco
```

#### Etc
```tree```, ```watch```, ```hub``` ...



### RVM 설치하기
```SHELL
$ \curl -L https://get.rvm.io | bash -s stable --rails --autolibs=enable
```   
출처 : <http://www.moncefbelyamani.com/how-to-install-xcode-homebrew-git-rvm-ruby-on-mac/>


***
## dotfiles 적용 (for bash)
.files, including ~/.osx — sensible hacker defaults for OS X

<https://github.com/mathiasbynens/dotfiles>

기본적으론 dotfiles 를 사용하고,
**.extra** 에 확장 또는 덮어쓸 명령을 추가한다.

My Extra Style :  
<https://github.com/rkJun/dotfiles/blob/master/.extra>

## dotfiles 적용 (for zsh)
준비중



***
## Homebrew-cask 설치

a friendly homebrew-style CLI workflow for the administration of Mac applications distributed as binaries

<https://github.com/phinze/homebrew-cask>

### Homebrew cask 로 application 설치

#### Browser 

- ##### 구글크롬
$```brew cask install google-chrome``` 

- ##### firefox
$```brew cask install firefox```


#### Terminal

- ##### iterm2
$```brew cask install iterm2```


#### Editor

- ##### Sublime Text 
$```brew cask install sublime-text```

- ##### MacVim
$```brew cask install macvim```

- ##### Haroopad
$```brew cask install haroopad```

 
#### IDE

~~##### - Eclipse (Standard)~~  
~~$```brew cask install eclipse-ide```~~

#### Tools

##### - XMind
$```brew cask install xmind```

##### - Caffeine
$```brew cask install caffeine```

#### 그외

$```brew cask install alfred```

$```brew cask install app-cleaner```

$```brew cask install coconutbattery```

$```brew cask install dropbox```

$```brew cask install mplayerx```

~~$```brew cask install spectacle```~~

$```brew cask install transmission```

$```brew cask install vlc```

$```brew cask install virtualbox```

$```brew cask install f-lux``` : Better lighting for your Mac

$```brew cask install bettertouchtool``

$```brew cask install diffmerge``

$```brew cask instlal cakebrew```


#### 압축해제 프로그램

Bandizip X - http://www.bandisoft.co.kr/bandizip/x/

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

3. 개발자에게 추천하는 OS X 훑어보기(QuickLook) 플러그인 6종 + α  
   <http://macnews.tistory.com/830> ![macnews icon][mnfavi]

4. 한영/영한사전 기능 추가 경로 (OSX 10.8 이하만. OSX 10.9 부터는 기본 내장)  
  /Users/`whoami`/Library/Dictionaries

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

#### Package Control 설치

* https://sublime.wbond.net/installation

#### 환경설정파일

* [전체](https://gist.github.com/rkJun/5733996)
   - [Default (OSX).sublime-keymap](https://gist.github.com/rkJun/5733996#file-default-osx-sublime-keymap)
   - [Package Control.sublime-settings](https://gist.github.com/rkJun/5733996#file-package-control-sublime-settings)
   - [Preferences.sublime-settings](https://gist.github.com/rkJun/5733996#file-preferences-sublime-settings)

[st]: http://sublimetext.com

### NTFS 외장하드 사용하기

[OS X 에서 NTFS 쓰기. FUSE for OS X, 그리고 NTFS-3G](http://rkjun.wordpress.com/2013/07/14/os-x-%EC%97%90%EC%84%9C-ntfs-%EC%93%B0%EA%B8%B0-fuse-for-os-x-%EA%B7%B8%EB%A6%AC%EA%B3%A0-ntfs-3g/)

또는,

[How to Write to NTFS External Disk Drives from OS X 10.8 Mountain Lion](http://crosstown.coolestguyplanettech.com/os-x/44-how-to-write-to-a-ntfs-drive-from-os-x)  
brew 로 설치하기 (fuse4x, ntsfs-4g)


### 추가폰트 적용
서체관리자
* 나눔고딕코딩  
   <http://dev.naver.com/projects/nanumfont>
* 나눔바른고딕
* 주아체
* 한나체
* Monaco for Powerline
