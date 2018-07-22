# AWS CodeCommit

AWS CodeCommit 은 간단히 말해 Private git repository 입니다.

별도의 git repository 를 구성할 필요도 없고, github 의 private repository 보다 [저렴](https://aws.amazon.com/ko/codecommit/pricing/)해서 쓸만합니다.

## 참조사이트

- https://docs.aws.amazon.com/codecommit/latest/userguide/setting-up-gc.html

## 1. IAM 에서 codecommit 용 user 생성

- IAM 서비스로 이동

- 사용자 > 사용자 추가

- AWS 콘솔에 액세스 유형 ```프로그래밍 방식 액세스``` 을 선택합니다.

- 권한 : ```기존 정책 직접 연결``` 은 선택하고, ```AWSCodeCommitFullAccess``` 를 선택합니다.

- 액세스키를 csv 로 다운받게 되는데 잘 보관해야 합니다.

- 사용자 목록에서 생성한 계정을 선택하고 보안 자격 증명 탭에서 ```AWS CodeCommit에 대한 HTTPS Git 자격 증명``` 에서 자격증명을 생성합니다.

## 2. repository 생성

- CodeCommit 서비스로 이동

- 신규 리포지터리 생성

- HTTPS URL 복사

## 3. git 설정

복사한 URL 을 복사한다.

```sh
git clone https://git-codecommit.us-east-2.amazonaws.com/v1/repos/MyDemoRepo my-demo-repo
```

아이디 비밀번호는 git 자격증명에서 생성된 아이디/비밀번호를 입력해준다.
