# EBS (Elastic Block Store)

- EC2에 attach(연결)해서 쓸 수 있는 block storage를 의미한다.

- 단일 가용 영역 내에서 여러 서버에 걸쳐서 복제된다.

- 특정 시점에 대한 볼륨 스냅샷을 만들 수 있다. (스냅샷 : 백업 파일 개념)  
  : S3라는 객체 기반 스토리지에 저장되며 복수계의 가용 영역에 걸쳐 자동으로 복제된다.

- 한 개의 EBS를 여러 EC2 인스턴스에 attach하는 것은 불가능하지만, 한 개의 EC2에 여러 개의 EBS를 attach하는 것은 가능하다.
  즉, 컴퓨터 용량을 늘리기 위해 SSD를 여러 개 연결할 수 있지만 하나의 SSD를 여러 컴퓨터에 동시에 연결할 수 없다는 것과 같다.

```
볼륨 (Vloume)
- 가장 기본적인 형태로 EC2에 바로 attach 가능

스냅샷 (Snapshot)
- 볼륨의 특정 시점을 그대로 복사하여 저장한 파일
- 스냅샷을 이용하여 볼륨 및 AMI(Amazon Machine Image) 생성 가능

AMI (Amazon Machine Image)
- OS가 설치된 형태의 이미지 파일
- AMI를 이용하여 EC2 인스턴스 생성 가능

IOPS(Input/Output Operations Per Second)
- 저장 장치의 성능 측정 단위
- 16KB 단위로 처리됨
- 추가 비용을 지불하여 더 높은 IOPS의 EBS를 생성할 수 있음
```

---

### 1. EC2 인스턴스 생성하기 (서울 리전, Ubuntu, t2.micro)

<img width="1715" alt="EBS-1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/d54f0a5a-b2cb-4696-a181-88b64207bbfc">

### 2. EBS 볼륨 생성 하기 (EC2 인스턴스와 같은 리전+가용영역, 용량은 8GB)

<img width="1718" alt="EBS-2 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/21acd08c-9473-420e-850d-154ff200c466">

### 3. EC2 인스턴스에 EBS 볼륨 연결하기

<img width="1721" alt="EBS-3" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/6381f10a-ecf1-4556-aa75-3112a992c6a7">

### 4. EC2 인스턴스에서 EBS 볼륨 제거하기

<img width="1718" alt="EBS-4" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/a9f90fa6-cf1d-4579-9d7d-dc2039813f5f">

### 5. EBS 볼륨 삭제하기

<img width="1718" alt="EBS-5" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/0deac4ad-0a90-4e58-84eb-8cae29ca6243">

### 6. EC2 인스턴스 종료하기

<img width="1717" alt="EBS-6" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/11345b4d-50e2-4c6d-abfd-e3f7f54fc895">
