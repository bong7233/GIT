# Git tag
특정 커밋에 버전을 기록할 때 사용하는 기능으로 릴리즈 버전을 기록할 때 주로 사용된다.
- Lightweight Tag : 버전만 기록하는 태그
- Annotated Tag : 태그를 생성한 유저,이메일,태그생성날짜,태그메세지를 함께 기록하는 태그
<br>


## Release
생성한 태그를 기반으로 Github에서 release 버전을 기록 할 수 있다.  
레포화면의 우측 Releases -> Create a new release를 클릭해 생성 한다.  

여기서 원하는 버전의 태그와 태그 설명을 설정 할 수 있고 pre-release 기능으로 임시 릴리즈상태로 만들기도 가능하다.  

결국 다른 사람이 이 레포를 들어왔을 때 한눈에 어떤 버전인지 알 수 있다.

<br>

## Git tag 생성
Github 의 repository의 Release 에서도 편하게 생성, 설정이 가능하지만, 터미널에서도 생성,푸시하는 법을 알고있어야 한다.  

- git tag \<tag name> : 태그를 생성 (-a 옵션으로 Annotated 태그도 생성 가능)  
- git tag : 생성된 태그 확인 (git log 로도 커밋에 태그가 등록된것을 확인할 수 있음)
- git show \<tag name> : 태그 상세내용 확인
- git push origin \<tag name> : 생성한 태그 깃헙에 등록

