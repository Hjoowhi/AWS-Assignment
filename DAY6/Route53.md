# Route 53

**DNS (Domain Name System)**  
도메인 이름을 IP 주소로 바꿔주는 시스템

|도메인 이름|IP 주소|
|:---:|:---:|
|google.com|172.217.31.174|
|amazon.com|176.32.103.205|
|github.com|192.30.255.112|

**도메인 이름과 IP 주소가 맵핑된 것을 레코드라고 한다.**

---

### Route 53
- 클라우드에서 사용하는 DNS (Cloud DNS)
- AWS의 서비스들과 쉽게 연동하여 사용할 수 있는 DNS라 할 수 있다.
- 클라이언트의 요청을 AWS에서 실행되는 인프라에 효과적으로 연결해서 사용할 수 있다.  
  : EC2 인스턴스, ELB 로드밸런서, S3 버킷, CloudFront 배포 등
- AWS 외부의 인프라로 라우팅할 때에도 사용할 수 있다.

### Route 53 기본 개념

**‣ 호스팅 영역 (Hosted Zone)**
- 레코드의 컨테이너로서 두 가지 유형이 존재한다.
- 퍼블릿  
  : 인터넷에서 트래픽을 라우팅하고자 하는 방법을 지정하는 레코드를 포함
- 프라이빗  
  : VPC에서 트래픽을 라우팅하고자 하는 방법을 지정라는 레코드를 포함

**‣ 레코드 (Record)**
- 도메인과 연결된 IP 주소
- 특정 도메인과 그 하위 도메인의 트래픽을 라우팅하는 방식에 대한 정보를 담고 있다.
- 호스팅 영역과 해당 도메인의 이름은 동일하다.

### Route 53 관련 용어
- DNS 쿼리 (DNS Query)  
  : 도메인 이름을 IP 주소로 변환하는 요청
   
- A 레코드 (Address Record)  
  : 도메인 이름과 IP 주소를 맵핑하는 레코드  
  : A는 주소(Address)를 의미

- DNS 장애 조치 (Failover)  
  : 서버 또는 ELB에 장애가 발생할 경우 다른 대체 위치로 라우팅 해주는 기능
  
---

### 1. 호스팅 영역 생성하기

<img width="1759" alt="route53-1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/48c0be58-6330-4c8c-9439-030ca5fefde9">

### 2. A 레코드 추가하기

<img width="1757" alt="route53-2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/3ac6f0ef-8030-4e78-8f07-d13524ad7e8c">

### 3. CNAME 레코드 추가하기

<img width="1741" alt="route53-3" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/87efa0c1-3fa8-4ce3-ae39-ad1f42f48704">

### 4. NS, SOA 레코드를 제외한 모든 레코드 삭제하기

<img width="1739" alt="route53-4" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/63ec9007-1425-46f1-9346-c0aa1041e5ed">

### 5. 호스팅 영역 삭제하기

<img width="1743" alt="route53-5" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/99e3524e-0e5f-4754-88d4-1169ad2db334">
