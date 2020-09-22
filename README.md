# 2020_MUSAT_Tutoring
오픈소스 소프트웨어 이해와 실습 튜터링 (예시용)

MUSAT!(Most helpful Ubuntu Special Activity Training)
특별과정에 오신 여러분들 환영합니다!

# Git/Github 학습하기에 앞서 준비해야 할것들

- Git Bash PC에 설치
- VSCODE PC에 설치
- Github 계정 가입

## Git/Github 학습하기에 앞서 튜터의 하고싶은말

## "Git/Github를 처음 사용해본 튜티들은 생소한 내용이기에 따라오기에 많이 어려울 수 있습니다. 그러니, Git/Github 학습주차를 늘려서라도 천천히 진행하겠습니다. "

# Git 이란?

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5b545ed5-0c21-4e51-bc0d-3ea811f49200/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5b545ed5-0c21-4e51-bc0d-3ea811f49200/Untitled.png)

로컬 PC 파일의 변경사항을 추적하고 여려 명의 사용자들 간에 해당 파일들의 작업을 조율하기 위한 분산 버전 관리 시스템

# Github?

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ac43e478-d07f-46e0-915c-cb6197036e3b/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ac43e478-d07f-46e0-915c-cb6197036e3b/Untitled.png)

- 클라우드 방식으로 관리되는 버전 관리 시스템(VCS)
- 자체 구축이 아닌 빌려쓰는 클라우드 개념 ⇒ 쉽게 말하면 구글드라이브? iCloud 같은거??

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/376d0f36-d42b-4eb4-a9db-b86bc9e45a7d/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/376d0f36-d42b-4eb4-a9db-b86bc9e45a7d/Untitled.png)

### Git 명령어로 로컬 PC에서 작업 후, Github라는 서버로 code 들을 Upload 혹은 download하여 쓴다. (다른 사용자와 협업을 위해서)

### Github외에도 Gitlab이나 비트버킷과 같은 다른 서비스들도 존재한다.

### 향후, 실무에서 Github외에 다른 서비스를 사용할 수도 있지만, 현재 우리가 주로 사용할 것은 Github이니 Github를 배워보자!

---

# Git/Github 용어

(용어 외운다고 무리 하지말고 부담가지지 말기! 뒤에 내용들 보면서 천천히 같이 이해하기!)

- 레포지토리(Repository): 원격 저장소, PC가 아닌 서버의 저장소
- 커밋(commit): 파일을 추가하거나 변경 내용을 저장소에 저장하는 작업
- 푸시(push): 파일을 추가하거나 변경 내용을 원격 저장소에 업로드하는 작업
- 풀(Pull): git server에서 최신코드 받아와서 merge하기
- 클론(clone): Repository를 로컬 PC로 가져오는 일
- 브랜치(branch): 독립적으로 어떤 작업을 하기 위한 개념
- fork: 타인의 레포지토리를 본인 계정의 레포지토리로 복제
- 태그(Tag): 커밋을 참조하기 쉽도록 알기 쉬운 이름으로 이름을 붙이는 것

    ⇒ 여기에는 일반태그와 주석태그가 있다. 

- HEAD: 현재 가리키는 branch
- Tag: Commit을 참조하기 쉽도록 알기 쉬운 이름을 붙이는 것
- Rollback: 이전 버전으로 돌아가기

# Git/Github 명령어들

(이것도 외우려고 하지말고 뒤에 내용들 천천히 따라하면서 이해해요.)

- git 상태 확인하기

```bash
git status
```

- git 생성하기

```bash
git init
```

- git 코드 가져오기

```bash
git clone [Repository URL]
```

- 브랜치 선택하기

```bash
git checkout [branch_name]

git checkout -t [remote_path/branch_name] 원격 브랜치 선택하기

git checkout -b [branch_name] [base_branch] 브랜치 없으면 생성하면서 체크아웃
```

- git 서버에서 최신코드 받아와 merge 하기(최신화)

```bash
git pull
```

- git 서버에서 최신 코드 받아오기

```bash
git fetch
```

- 커밋

```bash
git commit -m "Message"
```

- git 서버에 code 업로드

```bash
git push
```

- git rebase

```bash
git rebase
```

- 특정 브랜치와 merge 하기(합치기)

```bash
git merge [branch_name]
```

- 수정한 코드 선택하기

```bash
git add [file_path]
```

- 브랜치 생성

```bash
git branch [branch_name] 브랜치 생성하기

git branch -r 원격 브랜치 목록보기

git branch -a 로컬 브랜치 목록보기

git branch -m [branch_name] [change_branch_name] 브랜치 이름 바꾸기

git branch -d [branch_name] 브랜치 삭제하기
```

- commit한 이전 코드 취소하기

```bash
git reset --hard HEAD^

git reset --soft HEAD^ //코드는 살리고 commit만 취소하기
```

- merge 취소하기

```bash
git reset --merge
```

- git 계정 Name 변경하기

```bash
git config --global user.name "user_name"
```

- git 계정 email 변경하기

```bash
git config --global user.email "user_email"
```

- 기타 등등...

# How to make Repository

1. Click 'New'

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e7e928ba-cfd8-4069-9534-d047d45729b2/11.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e7e928ba-cfd8-4069-9534-d047d45729b2/11.png)

2.  Write down 'Repository name' what you want

Then, click 'Create Repository'

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/63508e47-b355-4c6d-828d-9f06350ed4c1/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/63508e47-b355-4c6d-828d-9f06350ed4c1/Untitled.png)

3. You can see your repository

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/94103f2d-f569-427a-95c6-947b030b4189/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/94103f2d-f569-427a-95c6-947b030b4189/Untitled.png)

(여기에 PC와 연동하는 방법이 친절히 설명되어 있다.)

# Basic Github Usage Pattern

### (1안)

ps. 처음이라 조금 어려울 수 있어요. 

1. PC 폴더에서 '여기에 Git을 쓸꺼다 명령'

```bash
git init
```

2.  Coding

```python
print("helloWorld!")
```

3. 변경한 파일 중 올리길 원하는 것만 선택

```bash
git add [파일명]

or

git add .
(전체 add)
```

4. 선택한 파일들을 한 덩어리로 만들고 설명 적어주기

```bash
git commit -m "Write down what you want "
```

5. GitHub 사이트에서 Repository 만들기

⇒ How to make Repository 참조

6. PC 폴더에 Github Repository 주소 알려주기

```bash
git remote add [origin] [http://github.com/Username/Repositoryname.git]

//여기서 []부분에 해당되는 내용으로 수정 해주면 됨
(명령어에 '[]' 문자 안넣는건 다들 알죠?? 그냥 영역을 표시한거니 눈치챙겨!)
```

7. Github에 올리기

```bash
git push
```

(2~7)과정 반복

### (2안)

ps. 1안에 비해서는 쉬운! 통상적으로 이런 패턴으로 주로 써요! 

1. Repository 만들기

    ⇒ How to make Repository 참고

2. 로컬 PC에서 github의 Repository clone 하기

```bash
git clone [url]
```

3. Coding

```cpp
#include<iostream>
using namespace std;

int main()
{
	cout<<"Capt. Lee Guen"<<endl;
}
```

4. Add

```bash
git add . 

(add . 은 모든 파일들을 추가한다는 것이다.)
```

5. Commit

```bash
git commit -m "Write down what you want"
```

6. Push

```bash
git push
```

(2~6 과정 반복)⇒ 2~6 과정은 다른 개발자가 만들어놓은 Repository를 본인의 PC로 가져오는 방식과 같습니다

```bash
git pull
```

### 둘 중 하나 마음에 드는 방법 시도하면 되요!

(Github Repository 관리권한 주는 방법 설명하기+ Github 페이지 보는법도!)

## What is branch?

(브랜치 만드는 법 설명, 브랜치 트리로 과정 설명)

브랜치(branch): 독립적으로 어떤 작업을 하기 위한 개념

처음 Repository를 만들면  master 라는 브랜치가 만들어 진다. 

혼자만의 Repository의 경우 master라는 하나의 브랜치에서 작업을 해도 무방하다.

다만, 버전관리 혹은 팀원들과 협업을 하게 될 경우, 본인의 작업영역이 아닌 다른 영역을 임의로 건드려서 프로젝트에 혼란이 오는 불상사가 일어날 수 있다. 

그래서, 브랜치를 사용하여 독립적으로 작업을 할 수 있는 환경을 구축한다. 

ex. 키썸과 헤이즈가 한 레포지토리에서 작업을 하려고 한다.  이때, 작업간 둘의 혼선을 막기 위해  각자의 브랜치를 만들어  독립적인 환경을 구축하여 작업한다.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/032aba69-518d-4ece-a6e9-d47af9071d91/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/032aba69-518d-4ece-a6e9-d47af9071d91/Untitled.png)

혹은,  배포용-테스트용 이렇게 브랜치를 나누어서 작업을 하기도 한다.

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6a9967d8-04b3-479c-8c7e-b2717223129c/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6a9967d8-04b3-479c-8c7e-b2717223129c/Untitled.png)

여기서 의문점! origin/master와 master의 차이는??

- github에 올리려면 push작업을 한다고 했죠?

### How to make branch

```bash
git branch [branch name]

ex. git branch son
```

or

```bash
git checkout -b [branch name]
//원래 checkout 명령어는 아래 보면 알듯이 브랜치 바꿀 때 쓰는 명령어이다.
checkout 명령어에 -b 라는 옵션을 준다. (해당 브랜치 없으면 새로운 브랜치를 생성하는 옵션)

```

### How to change branch

```bash
git checkout [branch name]
```

(아래 페이지 켜놓고 설명하기)

visualizing-git([http://git-school.github.io/visualizing-git/#free-remote](http://git-school.github.io/visualizing-git/#free-remote))

### 브랜칭 전략

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bd3c359b-7e77-41e2-af72-915878942b88/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/bd3c359b-7e77-41e2-af72-915878942b88/Untitled.png)

(실무에서 사용하는 브랜치 전략)

참고 : 좋은 git 커밋 메세지를 작성하기 위한 7가지 약속
[https://meetup.toast.com/posts/106](https://meetup.toast.com/posts/106)

[참고사이트]

[https://medium.com/@pks2974/자주-사용하는-기초-git-명령어-정리하기-533b3689db81](https://medium.com/@pks2974/%EC%9E%90%EC%A3%BC-%EC%82%AC%EC%9A%A9%ED%95%98%EB%8A%94-%EA%B8%B0%EC%B4%88-git-%EB%AA%85%EB%A0%B9%EC%96%B4-%EC%A0%95%EB%A6%AC%ED%95%98%EA%B8%B0-533b3689db81)
[https://tagilog.tistory.com/377](https://tagilog.tistory.com/377)
[https://medium.com/@flyingSquirrel/git-rebase-하는-방법-ce6816fa859d](https://medium.com/@flyingSquirrel/git-rebase-%ED%95%98%EB%8A%94-%EB%B0%A9%EB%B2%95-ce6816fa859d)
[https://cyberx.tistory.com/96](https://cyberx.tistory.com/96)
