# SSH 연결 관련 팁

## SSH 키 생성하기

```
# Git bash에서 
$ ssh-keygen
$ ls ~/.ssh
```

```
# Windows CMD에서 
$ ssh-keygen
$ dir %userprofile%\.ssh
```

간혹, 반드시 PuttyGen을 사용해야 한다면 PuttyGen으로 생성한 .ppk파일을 'Export OpenSSH Key'를 통해 .pub파일로 변환한 후 등록하세요.
Bee는 OpenSSH 만을 지원합니다.

## PuTTY 연결 방법 (원격 터미널)

1. PuTTY 실행

2. Host Name, Port 입력 (Connection type: SSH)
  예시)
    - Host Name: soonbum-jeong-poip.bee0.lge.com
    - 58873

3. Connection > Data > Auto-login username 입력
  예시) worker

4. Connection > SSH > Auth > Credentials에서 공개키 파일 추가
  - Private key file for authentication: id_rsa.ppk 파일 경로 찾아서 입력
  - PEM 파일만 있을 경우 PuTTY Key Generator로 변환해서 PPK 파일을 생성할 것

5. 이제 연결이 가능합니다.

## WinSCP 연결 방법 (원격 파일 업로드/다운로드)

1. 파일 프로토콜: SFTP

2. 호스트 이름, 포트 번호 입력

3. 사용자 이름 및 패스워드 입력

4. 고급 > SSH > 인증 > 개인키 파일에 id_rsa.ppk 파일 추가

5. 저장 후 로그인하면 됩니다.
