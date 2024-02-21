# AWS SDK, CLI (공유 자격 증명 설정)

### SDK (Software Development Kit)
- 소프트웨어 개발 키트  
  : 애플리케이션을 만들기 위한 소프트웨어 개발 도구의 집합

### AWS SDK
- 내가 만드는 애플리케이션에 AWS를 연동하기 위한 개발도구의 집합
- 다양한 언어와 프레임워크를 위한 SDK를 제공한다.
- 웹과 모바일 앱을 위한 SDK도 별도로 제공한다.
- 개발하려는 플랫폼에 맞는 SDK를 선택하여 사용 가능하다.

### CLI (Commannd Line Interface)
- 명령행 도구  
  : 터미널을 통해 명령을 실행할 수 있게 해주는 도구

### Shared Credentials (공유 자격 증명)
- 컴퓨터에 AWS 지격 증명을 설정함으로써, 해당 컴퓨터를 사용하는 사람은 별도의 설정 없이 SDK나 CLI를 사용하여 AWS 섭스를 사용할 수 있도록 해준다.
- AWS를 사용해서 서비스를 개발하는 경우, 거의 필수적으로 설정해야 한다.
- https://docs.aws.amazon.com/ko_kr/sdkref/latest/guide/file-format.html

- **공유 자격 증명 파일 위치**  
  : config, credential 둘 중 하나만 생성하면 된다.

  |운영 체제|기본 위치 및 파일 이름|
  |:---:|:---:|
  |Linux 및 macOS|~/.aws/config|
  ||~/.aws/credentials|
  |Window|%USERPROFILE%₩.asw₩config|
  ||%USERPROFILE%₩.aws₩credentials|

---

### 1. IAM 사용자 생성하기 (S3ReadOnlyAccess 권한 포함)

<img width="1766" alt="SDK_CLI-1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/89f87a78-2045-4712-9f66-9974b9d8dc06">

<img width="1758" alt="SDK_CLI-1 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/63a2fc6f-97d6-4c3a-b467-f80dfa9715d6">

### 2. 생성한 IAM 사용자에 액세스 키 만들기 (CLI 용도)

<img width="1766" alt="SDK_CLI-2 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/fc9e7a77-b9cd-4a0d-abc0-c25d5f03cdee">

<img width="1767" alt="SDK_CLI-2 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/41da9f3d-794f-4982-8a78-a9d0da39e7ad">

### 3. 생성한 액세스 키를 사용하여 사용 중인 컴퓨터에 공유 자격 증명 설정하기

<img width="905" alt="SDK_CLI-3 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/9ed7432a-a6cb-4cd5-abb9-3c9a967816d0">

<img width="878" alt="SDK_CLI-3 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/a64c7fdc-aa6c-4c78-bfab-ad70f8edcedd">

<img width="905" alt="SDK_CLI-3 3" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/43210b42-8f7e-42f2-9a1a-27298fbd3850">

<img width="889" alt="SDK-CLI-3 4" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/b2e0d118-47a0-442e-8bf3-2ae25bd28e81">

<img width="889" alt="SDK_CLI-3 5" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/3b76f766-25a6-448c-8611-9528d00319ee">

<img width="776" alt="SDK_CLI-3 6" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/f66fa1dd-2e58-4fd6-8336-ca4925eb1ce1">

<img width="845" alt="SDK_CLI-3 7" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/95b03e0b-d37e-4ab7-9d77-fefdd771a611">

<img width="776" alt="SDK_CLI-3 8" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/008b708f-febf-48e9-a04e-aac8c250b1be">

<img width="1687" alt="SDK_CLI-3 9" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/383e4083-ff56-4950-a64b-d8aad68f40f8">

<img width="773" alt="SDK_CLI-3 9-2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/fba51a11-bf06-4b3e-b8e5-b25695cd65f3">

### 4. AWS CLI를 설치하여 S3 명령어 테스트 해보기

https://docs.aws.amazon.com/ko_kr/cli/latest/userguide/getting-started-install.html

<img width="735" alt="SDK_CLI-4" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/c4a22448-1cf9-4d13-b66c-fd82df054c1d">

<img width="777" alt="SDK_CLI-4 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/d8ba0ccc-9985-438d-8682-c6c30cea9ec8">

<img width="1688" alt="SDK_CLI-4 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/59a953b9-f46a-420e-829b-23cb962561da">

<img width="777" alt="SDK_CLI-4 3" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/a1389e76-5691-40c5-9caa-130ca95848e0">

<img width="1685" alt="SDK_CLI-4 4" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/d633434d-8978-4647-b213-0e84bb874068">

<img width="773" alt="SDK_CLI-4 5" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/630b1928-fc00-4e6a-ae67-3cb4d77b3542">

### 5. 공유 자격 증명 제거하기

<img width="780" alt="SDK_CLI-5 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/d03bfeca-cb38-401a-ac60-74c7b72b4f9c">

<img width="1687" alt="SDK_CLI-5 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/04c34809-0cbd-4b1c-9310-52d17776d68f">

### 6. IAM 사용자 삭제하기

<img width="1690" alt="SDK_CLI-6" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/438a5a17-e5aa-467e-acf8-558d80d40dce">
