# Elastic IP (Elastic IP address)

- 클라우드 컴퓨팅을 위해 고안된 정적 IPv4 주소  
  (IPv4 : 인터넷 프로토콜 버전 4, 4자리로 구분된 흔히 사용하는 IP주소 | 예 - 123.123.123.123)

- 탄력적 주소는 AWS 계정과 연결되기에, 각 계정별로 할당받을 수 있는 탄력적 주소의 개수가 정해져 있다.
  (모든 AWS 계정은 Elastic IP 주소가 리전당 5개로 제한된다.)

```
‣ AWS에서 Elastic : 여기저기 붙였다 뗐다 할 수 있는 성질, 다른 aws 서비스와 연동시키거나 연동을 해제한다.  
‣ AWS의 서비스명에 Elastic이라는 단어가 들어갈 경우, 다른 서비스와 유연하게 연동해서 사용할 수 있다고 생각하면 된다.
```

---

### 1. EC2 인스턴스 생성하기 (서울 리전, Ubuntu, t2.micro)

<img width="1726" alt="ElasticIP-1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/a867bfac-2789-435c-8616-ff9b568d61ed">

### 2. Elastic IP 할당 받기

<img width="1724" alt="ElasticIP-2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/868e567d-cf4b-4c41-a239-bd6ee38a57a5">

### 3. 할당 받은 Elastic IP를 EC2 인스턴스에 연결하기

<img width="1726" alt="ElasticIP-3 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/9f987a96-24f7-4dcd-97ee-2db8f22cda26">

<img width="1725" alt="ElasticIP-3 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/dd7f1cf8-f644-47f2-af6d-88dee4be098c">

### 4. 연결한 이후 Elastic IP를 통해 ssh 접속하기

<img width="777" alt="ElasticIP-4" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/3d7cb6c1-f478-4869-a19c-d9ac19735641">

### 5. EC2 인스턴스에서 Elastic IP 연결 해제하기

<img width="1726" alt="ElasticIP-5" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/2272c777-ac9b-4957-9456-b63d629e2b0e">

### 6. 할당 받은 Elastic IP 릴리즈 하기

<img width="1724" alt="ElasticIP-6" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/6d63b191-a472-4152-a88c-8a400bbfc819">

### 7. EC2 인스턴스 종료하기

<img width="1726" alt="ElasticIP-7" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/655ecf3a-c040-413b-8df7-d6493b9b6214">
