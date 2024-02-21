# CloudFront

- AWS에서 CDN의 역할을 하는 서비스  
  : CDN(Content Delivery Network) = 컨텐츠를 전세계로 빠르게 전송할 수 있게 해주는 것
  
- 이미지, HTML 등의 컨텐츠를 캐싱하여 성능을 가속시킨다.
  
- 400개 이상의 전세계 수많은 엣지 로케이션(Edge Location)을 통해 컨텐츠를 빠르게 전세계로 전송할 수 있다.
  
- 글로벌 고속 백본 네트워크를 확보하고 있다.
  
- AWS 서비스와 클라우드 프론트 사이의 데이터 전송은 무료이며, DDoS 방어 또한 무료로 제공된다.  
  : AWS Shield Standard에 의한 L3/L4 DDoS 보호는 추가 비용 없이 포함된다.

### CloudFront 기본 용어

**‣ 배포 (Distribution)**  
- CloudFront의 가장 기본적인 단위
- 각 배포는 고유의 도메인을 가지게 된다.  
  :Route 53을 사용해서 자신이 구입한 도메일에 연결 가능

**‣ 오리진 (Origin)**
- 원본 파일을 가져오는 위치  
  : 기본 설정 : S3  
  : 커스텀 설정 : EC2, ELB, 외부 서버

---

### 1. S3 버킷 생성하기 (서울 리전)

<img width="1533" alt="CF-1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/52dd1902-8e71-452b-94f3-22c26d91cc20">

### 2. 생성한 버킷을 origin으로 하는 CloudFront 배포 생성하기 (원본 액세스 제어 설정 포함)

<img width="1717" alt="CF-2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/fb8db76b-7d65-4379-a10d-702a5f48a6d1">

### 3. 배포 생성 후 S3 버킷 정책 업데이트 하기 (CloudFront가 버킷의 모든 객체에 접근할 수 있도록)

<img width="1716" alt="CF-3 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/2433f09f-0493-4094-8cac-6dfdb9ecfb1c">

<img width="1750" alt="CF-3 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/2ddf7d9f-4ff1-445e-b7df-1aa4387b0dcd">

### 4. CloudFront 배포 도메인 이름으로 접속하여 객체가 잘 나오는지 확인하기

<img width="1830" alt="CF-4" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/ed0f54ca-c8ef-47e1-aa62-c189d607afb8">

### 5. CloudFront 배포 및 S3 버킷 삭제하기

<img width="1768" alt="CF-5 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/8e971e40-e99e-4a99-8e4e-5a8e437de361">

<img width="1768" alt="CF-5 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/e40ce085-b2d8-4e7b-9fc4-122ece325bda">

<img width="1765" alt="CF-5 3" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/84461633-6c0b-4a36-8761-b09a3b77c62c">
