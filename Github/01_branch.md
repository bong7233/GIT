# 브랜치 전략
Git 과 Github의 브랜치전략 차이에대해 알아야 한다.  

## Git Flows
Git Flow 는 로컬중심 브랜치전략이다.  
일반적으로 사용되는 브랜치는 main(master), develop, release, feature, hotfix 등이 있다.  

- main(master)  
배포의 기준이되는 브랜치로 , Release Tag를 기록한다.  
배포용이기 때문에 main에 직접 커밋하거나 머지하면 안되지만 예외적으로 hotfix 브랜치는 main에 바로 머지할수도 있다.

- develop  
개발이 이뤄지는 브랜치로 동시에 작업하게되면 conflict가 발생할 수 있다.  
그래서 실제로는 feature브랜치에서 작업 후 develop 에 머지하는 방식으로 개발프로세스가 진행된다.  

- release  
실제 배포를 하기위해 준비하는 브랜치로 develop 브랜치에서 다음 릴리즈를 위한 개발이 끝나면 여기로 분기하여 버그픽스와 리팩토링을 진행한다.  
배포준비가 완료되면 그떄 main 브랜치로 머지한다.  

- hotfix  
배포가 완료된 main 브랜치에서 심각한 버그가 발생했을 때 사용하는 브랜치다.  
기본적으로 main에는 직접 커밋을 할 수 없으므로 핫픽스 브랜치에서 문제를 해결 후 main,develop에 머지한다.  

- feature  
개발 작업의 중심이 되는건 develop이지만, 실제 기능을 구현하는 브랜치는 feature다.  
이슈에 등록된 기능을 구현하거나 버그픽스,리팩토링 작업을 develop에서 분기된 feature에서 작업 후 머지한다.  

## Github Flows
Github Flow 는 remote 중심 브랜치전략이다.  
중심이되는 main 브랜치와 각각의 feature 브랜치로 구성된다.  
Git flow와 비교하면 main은 main,develop,release / feature는 feature,hotfix가 합쳐진 형태라고 보면 된다.  

작업한 내용을 수시로 remote로 push 하여 항상 최신상태를 유지한다. 이 부분이 리모트중심 브랜치전략의 핵심이다.  
develop이나 release 브랜치처럼 배포준비를 위한 브랜치가 따로 없기 때문에 main 브랜치에 머지하는 작업을 엄격하게 관리해야 한다.  



