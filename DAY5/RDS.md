# RDS (Relational Database Service)

- 관계형 데이터베이스 + DB와 관련된 모든 작업을 제공해주는 서비스

- Fully Managed Relational Database (완전 관리형 관계형 데이터베이스) 라고도 하며, 데이터베이스와 관련된 모든 작업을 다 해준다.

- 다양한 DB엔진을 제공한다.  
  : ORACLE, MySQL, PostgreSQL, MariaDB, Aurora 등

- 직접 하려면 번거로운 DB 이중화(Multi-AZ) 작업이나 Read Replica 생성도 손쉽게 할 수 있다.  
  : AZ(Availability Zone) = 가용 영역  
  : Multi-AZ = 복수계의 가용 영역에 DB 인스턴스를 둠으로써 이중화하는 것

- 인스턴스 확장을 쉽게 할 수 있다.

---

### 1. RDS 인스턴스 생성하기 (서울 리전, MySQL, db.t3.micro)

<img width="1751" alt="RDS-1 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/5449fb70-572d-413e-b0e9-74c9dd82f450">

<img width="1751" alt="RDS-1 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/e5994e6c-9dab-41c9-8416-fd7446a83c4d">

<img width="1750" alt="RDS-1 3" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/b8fc3f4f-dea3-4157-b8f6-49ecff352bc4">

### 2. MySQL Workbench를 사용하여 RDS 인스턴스에 접속하기

- Hostname : 엔드포인트

- Username : 마스터 사용자 이름

- Password : 마스터 암호

<img width="805" alt="RDS-2 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/7069351b-34e1-4c97-b39a-8f930f9a9064">

<img width="1881" alt="RDS-2 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/13263480-610e-4d86-978d-a3ae62c0c8cb">

<img width="1783" alt="RDS-2 3" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/42393e68-c8cb-448b-af32-60ebe4a8f98d">

### 3. RDS 인스턴스 삭제하기

<img width="1764" alt="RDS-3" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/acdaf1ee-6e16-40e3-bac0-987825949cdd">
