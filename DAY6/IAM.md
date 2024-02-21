# IAM (Identity and Access Management)

- AWS 서비스와 리소스에 대한 권한(액세스)을 관리하기 위한 서비스  
  : IAM 사용자 및 그룹을 만들어서 관리한다.
- 권한을 사용해서 AWS 리소스에 대한 액세스를 허용하거나 거부할 수 있다.
- 추가 비용 없이 제공된다.  
  : 사용자가 사용한 다른 AWS 서비스에 대해서만 요금이 부과된다.
- Key를 발급함으로써 AWS 외부에서 API로 접근할 수 있다.

### IAM 기본 개념

- **User**  
  : AWS 서비스 사용자 (사람 또는 외부 애플리케이션)

- **Group**  
  : User들의 집합

- **Role**   
  : AWS의 작업과 리소스에 대한 액세스를 부여하는 권한 세트

- **Policy**  
  : 특정 AWS 요소의 특정 기능을 사용하기 위한 정책

- **Permission**  
  : Policy들의 집합

### IAM 사용 방식

- **Root 계정 노출없이 사용자에게 제한적인 권한(Role)을 부여하고 싶을 때 사용한다.**
  
- **Programmatic Access**  
  : AWS SDK등을 이용하여 AWS 서비스에 API로 접근하는 방식  
  : Access key ID, Secret access key로 구성된 키가 발급된다.  
  : 일반적으로 많이 사용하는 방법이다.

- **AWS Management Console Access**  
  : 전용 Console login link로 접속하는 방식  
  : AWS Management Console에 제한된 로그인이 필요할 때만 사용한다.

---

### 1. IAM 사용자 생성하기 (Management Console 액세스, EC2ReadOnlyAccess 권한 포함)

<img width="1729" alt="IAM-1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/2cf0fd55-ee67-4ece-b168-e3a9562655f0">

### 2. 생성한 IAM 사용자로 AWS 콘솔 로그인하기

<img width="878" alt="IAM-2 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/dbba5b87-b735-4134-84d1-406e36959c25">

<img width="1720" alt="IAM-2 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/7ae6e149-7ba6-4f92-be5c-a96eee1f9e96">

### 3. EC2 페이지 접속해서 잘 나오는지 확인하기

<img width="1618" alt="IAM-3 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/4f900dc6-14c6-4239-9d65-b5d4d1b2ecbb">

<img width="1719" alt="IAM-3 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/d8943916-b5ff-4083-bdf0-701f6e328d89">

### 4. IAM 사용자 삭제하기

<img width="1719" alt="IAM-4 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/57fd9542-5047-429f-8b17-44a269af5cfc">

<img width="1716" alt="IAM-4 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/46cfa231-5e22-48cf-8fde-7051f31cc306">
