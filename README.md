# OS X First Settings of My Style

어느 웹 개발자의 개인 스타일 맞춤형 OS X 개발환경 세팅. **ver. rkJun**

[펭귄너구리](http://blog.doortts.com)님의 글(어떤 개발자의 맥환경 <https://github.com/doortts/env-of-mac>)
을 보고, 저도 개인적인 정리 차원에서 올려둡니다.

## 시스템환경설정

- 핫코너
- 키보드
  - 키반복 최대한 빠르게, 반복지연시간 최대한 짧게 설정.
  - 조합키 - Caps Lock 키를 ^Control 키로 변경
- iCloud 설정 등
 
## AppStore
- Update
- *iPhoto, iMovie*
- *twitter*
- *Xcode*
  - *Command Line Tools* (Xcode - Preferences - Downloads)

## 구름입력기 설치
<http://gureum.org/> 세벌식 사용자 또는 vi 사용자에게 유리

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

#### mongodb
$```brew install mongodb```

### RVM 설치하기
$``` \curl -L https://get.rvm.io | bash -s stable --rails --autolibs=enable```   
출처 : <http://www.moncefbelyamani.com/how-to-install-xcode-homebrew-git-rvm-ruby-on-mac/>


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

#### Browser 

##### - 구글크롬
$```brew cask install google-chrome``` 

###### - 구글크롬 canary 
$```brew cask install google-chrome-canary```

##### - firefox
$```brew cask install firefox```


#### Terminal

##### - iterm2
$```brew cask install iterm2```


#### Editor

##### - Sublime Text 
$```brew cask install sublime-text```

##### - MacVim
$```brew cask install macvim```

##### - Mou : Markdown Editor
$```brew cask install mou```

#### IDE

~~##### - Eclipse (Standard)~~  
~~$```brew cask install eclipse-ide```~~

#### Tools

##### - Xtra Finder
$```brew cask install xtra-finder```

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

$```brew cask install spectacle```

$```brew cask install transmission```

$```brew cask install vlc```

$```brew cask install virtualbox```

$```brew cask install f-lux``` : Better lighting for your Mac

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

* Sublime Package Control 설치 -Sublime Text 2 에서
View - Show console (단축키 ^+`) 에서 아래 명령 실행

   참조 : 생활코딩 <http://opentutorials.org/module/406/3602>  
   참조 : wbond.net <http://wbond.net/sublime_packages/package_control/installation>


```
import urllib2,os; pf='Package Control.sublime-package'; ipp=sublime.installed_packages_path(); os.makedirs(ipp) if not os.path.exists(ipp) else None; urllib2.install_opener(urllib2.build_opener(urllib2.ProxyHandler())); open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read()); print('Please restart Sublime Text to finish installation')
```

* Sublime Package Control 설치 - Sublime Text 3 에서

   참조 wbond.net <http://wbond.net/sublime_packages/package_control/installation#ST3>


[st]: http://sublimetext.com

### NTFS 외장하드 사용하기

[OS X 에서 NTFS 쓰기. FUSE for OS X, 그리고 NTFS-3G](http://rkjun.wordpress.com/2013/07/14/os-x-%EC%97%90%EC%84%9C-ntfs-%EC%93%B0%EA%B8%B0-fuse-for-os-x-%EA%B7%B8%EB%A6%AC%EA%B3%A0-ntfs-3g/)

또는,

[How to Write to NTFS External Disk Drives from OS X 10.8 Mountain Lion](http://crosstown.coolestguyplanettech.com/os-x/44-how-to-write-to-a-ntfs-drive-from-os-x)  
brew 로 설치하기 (fuse4x, ntsfs-4g)


### 추가폰트 적용
서체관리자 실행후 폰트 파일 복사

* 나눔고딕코딩  
   <http://dev.naver.com/projects/nanumfont>
