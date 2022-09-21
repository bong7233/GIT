# Pull request

머지 작업을 진행하기 전 팀원에게 코드를 받는 단계이다.  
reviewr, assignee를 반드시 지정하고, 가능하다면 Label도 붙여야 한다.  

<br>

## PR Template

대략적인 내용(overview), 변경된 부분(change log), 리뷰어가 참고할 사항(to reviewer), 관련된 이슈(issue tag)를 기록한다.  

이슈태그에 특정 키워드를 적어두면, 해당 PR이 default branch에 머지될 때 연관된 이슈가 자동으로 닫히도록 할 수 있다. (close, fix, resolve 등)  
단, PR은 .github 경로에 가서 직접 md 파일을 주가해줘야 한다.  
```markdown

## Overview

## Change log

## To Reviewer

## Issue Tags
Closed | Fixed:
See also:
```

<br>

## PR 체크
files chaged 에 들어가면 코드 왼편의 숫자부분에 마우스를 올려 코멘트를 남길 수 있다.  
이후 코드리뷰가 마무리되면 Finish your review 버튼을 클릭해 리뷰를 끝낼 수 있다.  

코드리뷰에서 approve 를 받으면 코드를 대상 브랜치로 머지할 수 있다.  
이때 세가지 옵션이 있다.  
- create a merge commit : 머지 커밋을 추가로 남기고 머지
- Squash and merge : 커밋로그를 하나로 합치면서 머지
- Rebase and merge : 머지 커밋을 남지기 않고 기존 커밋로그를 유지한 채로 머지  





