## 📌 2021 - Socket Ransomware
## TCP/IP 학습을 위해 소켓을 이용한 랜섬웨어 🚨
#### Project nickname : 소켓 랜섬웨어
#### Project period : 2021.10.14~2021.12.14
-----------------------
## 💻 Description
Socket Ransomware 프로젝트는 시스템보안 과목에서 배운 SHA-256과 AES 암호화를 TCP 소켓 통신을 이용하여 실제로 구현해보기 위해 진행하게 되었습니다.

최근 강력한 보안 위협으로 주목 받는 랜섬웨어와 TCP 소켓 통신을 결합한 프로젝트로 랜섬웨어 공격의 동작 방식을 잘 보여주고 있습니다. 이를 통해 보안의 중요성을 다시 한번 인식할 수 있을 것이라고 생각합니다.

## ⚙ Environment

> C# .NET Framework
>
> MYSQL

## Main Function
### 암호화

- 클라이언트에서 서버로 접속할 때, MAC값을 서버에게 전달한다.
- 이 MAC값을 SHA-256 알고리즘을 이용하여 키를 생성한 후 클라이언트에게 전송한다. 생성된 키와 클라이언트 정보는 DB에 저장된다.
- 서버로부터 받은 키를 이용해 클라이언트는 AES 알고리즘을 이용하여 파일을 암호화한다.

### 복호화

- 클라이언트에서 결제를 완료한 후 서버에 복호화 키를 요청한다.
- 요청받은 서버는 DB에 저장되어 있는 복호화 키를 클라이언트에게 전송한다.
- 서버로부터 받은 키를 이용해 클라이언트는 AES 알고리즘을 이용하여 파일을 복호화한다.


## 🗂 System Structure

<img src="https://user-images.githubusercontent.com/83394485/176669961-6bb2a85c-af7b-4e81-a8bf-6e560b693f39.JPG" width="400"/>

## 🎥 Result
### 서버 

<img src="https://user-images.githubusercontent.com/83394485/176670854-783840b0-cf92-46c8-a46c-2b37b3a9b38a.png" height="400" width="800" />

### 클라이언트

<img src="https://user-images.githubusercontent.com/83394485/176670982-c7958709-b288-47f7-8dc1-be874df0d651.png" height="400" width="800" />

🚔본 Socket Ransomware 프로젝트는 학습용으로 만들어졌습니다.🚔
