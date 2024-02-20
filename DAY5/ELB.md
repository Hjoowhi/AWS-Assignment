# ELB (Elastic Load Balancing)

- 부하를 여러 개의 EC2에 골고루 분산시켜주는 역할을 한다.
  
- ELB는 리전별로 생성한다.
  
- 리전에 생성된 ELB는 여러 개의 가용 영역에 존재하는 EC2 인스턴스들의 부하를 분산시켜준다.  
  : 대상그룹이라 불리는 그룹에 속한 EC2 인스턴스들에게만 부하를 분산시키게 된다.  
  (대상그룹(Target Group) : 부하를 분산시킬 대상 인스턴스들이 속한 그룹)
  
- 여러 개의 가용 영역으로 부하를 분산시킬 수 있기에 가용 영역 하나가 통째로 중단되어도 정상적으로 운영할 수 있다.

  ```
  Load Balancing 알고리즘
  - 트래픽을 각 서버에 분배하는 방법 (빵을 나눠주는 방법)

  Health Check
  - 서버가 살아있는지 확인하는 것 (학생이 빵을 먹을 준비가 되었는지 목이 막혔는지 확인하는 것)
  - 만약 서버가 중단 되었다면 트래픽을 분해하지 않는다. (목이 막힌 학생에게 더 이상 빵을 주지 않는다.)

  Connection Draining (등록 취소 지연)
  - 사용자의 요청을 처리중인 서버를 곧바로 삭제하지 못하도록 방지하는 기능
  - Drain은 '물을 빼내다'라는 뜻을 가지고 있다.
  - 트래픽이 줄어서 늘렸던 인스턴스 중 몇 개를 삭제하려고 할 때, 삭제될 인스턴스에 연결 중인 사용자가 있을 수 있기 때문에 지정한 시간만큼 기다린 이후에 인스턴스를 삭제한다.

  Latency
  - Load Balancer와 서버 사이의 지연 시간
  ```

---

### 1. 로드밸런싱이 필요한 이유와 역할 설명해보기

**Load Balancing (부하 분산)**
- 서버에 요청이 과하게 많이 들어올 수 있기에 이 부하들을 여러 대의 서버로 잘 분산시켜 요청을 시간 내에 잘 처리할 수 있게 하는 것이다.
- 로드 밸런싱 알고리즘에 따라서 요청들을 분산시키고 타임아웃이라 불리는 제한시간 내 각 서버에서 처리한다.

**Load Balancer**
- 각 서버로 부하를 분산시켜주는 역할을 하는 것이다.
- 로드 밸런서가 클라이언트들의 요청을 각각의 서버(EC2)로 나눠준다.

**Load Balancing의 목적**
1. 성능 향상 (Performance)  
   : 로드 밸런싱을 적용하게 되면 클라이언트들의 수많은 요청들을 여러 대의 서버가 나눠서 처리하기 때문에 빠르게 응답해줄 수 있다.  
   : 같은 시간에 처리할 수 있는 요청의 개수가 확연하게 늘어나기 때문이다.

2. 안정성 향상 (Stability)  
   : 여러 개의 EC2 인스턴스가 죽어도 남은 EC2 인스턴스들이 클라이언트들의 요청을 처리해 줄 수 있기 때문이다.

3. 서버 장애 예방 (Backup Plan)  
   : 클라이언트들의 요청이 대량으로 몰랴오거나 여러 개의 EC2 인스턴스가 죽더라도 미리 계획해준 백업 플랜에 따라 EC2 인스턴스를 더 띄울 수 있기 때문이다.

4. 고가용성 (High Availability, HA)  
   : 서버가 오랜기간 동안 정상적으로 작동이 가능한 성질로, 가용성이 높다는 것은 장애가 나지 않고 지속적으로 서버가 정상적으로 작동한다는 것을 의미한다.  
   : 로드 밸런싱을 적용하게 되면 장애를 미리 대비할 수 있기 때문이다.

5. 성능 향상 기반 제공 (Performance Enhancement)  
   : 로드 밸런서가 성능 향상의 기반이 되기 때문에, 클라이언트의 요청이 갑자기 많아져도 EC2 인스턴스를 더 띄우고 로드 밸런서를 통해 부하를 분산시키기 때문이다.

### 2. EC2 인스턴스 생성하기 (서울 리전, Bitnami Wordpress, t2.micro)

<img width="1766" alt="ELB-1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/22b8f472-d0b1-4d83-9f2a-8477352b8672">

### 3. ALB 생성하기 (EC2 인스턴스와 같은 리전)

<img width="1741" alt="ELB-2 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/d43c5b98-7754-46cf-8ec2-372bf30548d5">

<img width="1764" alt="ELB-2 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/828b067d-e3f1-4819-bd87-b4c505129162">

<img width="1762" alt="ELB-2 3" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/a928dd8e-b3cc-44a2-b82d-913bd6a60195">

### 4. ALB의 주소를 통해 EC2 인스턴스에 접속하기

<img width="1765" alt="ELB-3 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/e9e16acc-337d-402c-a1e8-6c3466c6f80d">

<img width="1765" alt="ELB-3 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/8be63889-0988-4323-be5b-0718bbd3bdd9">

### 5. EC2 인스턴스 종료하기

<img width="1763" alt="ELB-5 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/916819bc-e1ff-4c7d-bf58-c53d898f7ec8">

<img width="1764" alt="ELB-5 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/069363b1-4ba4-42c4-a10a-3e4ea5272012">

<img width="1762" alt="ELB-5 3" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/e064562c-115e-40af-b12a-e50e56f2b60c">
