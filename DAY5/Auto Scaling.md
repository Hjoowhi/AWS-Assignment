# Auto Scaling

### 1. Auto Scaling이 필요한 이유와 역할 설명해보기

**🤔 Auto Scaling의 필요성**

보통의 경우 서버의 최대 용량은 고정되어 있는데, 서버로 들어오는 트랙픽의 양은 고정되어 있지 않는다. 따라서 갑자기 서버의 트래픽이 몰리게 되면 서버 용량 초과로 인해 서버에 장애가 발생하여 고객들에게 정상적인 서비스를 제공할 수 없게 된다.  
이러한 상황을 방지하고자 서버의 최대 용량을 확 늘려버리면, 평소 트래픽이 몰리지 않을 때에도 서버의 용량을 크게 유지해야 하기 때문에 낭비되는 자원이 많이 생기게 되어 비용적으로 굉장히 비효율적이다.

서비스를 안정적으로 제공하면서 낭비되는 자원이 없도록 비용 효율적으로 하기 위해 등장한 것이 Auto Scaling 이다.  
오토 스케일링을 사용하게 되면 실제 트래픽과 거의 유사한 수준으로 서버의 용량을 조절할 수 있다.  
따라서 트래픽이 늘어나도 서버의 용량이 자동적으로 늘어남으로써 안정적으로 서비스를 제공할 수 있으며, 
트래픽이 즐어들어도 서버의 용량도 자동으로 줄어듬으로써 낭비되는 자원이 생기지 않도록 할 수 있다.

**Auto Scaling을 사용하면 안정적이며 효율적으로 서버를 운영할 수 있다.**

**🤔 Auto Scaling의 역할 및 기본구조**

- 일반적으로 트래픽에 따라서 자동으로 서버의 개수를 조절해주는 기능이다.

- AWS 관점에서는 트래픽에 따라서 자동으로 EC2 인스턴스 개수를 조절해주는 기능이다.

- Auto Scaling은 ELB와 함께 사용된다.

- 기본 구조

  1. 클라이언트의 요청이 ELB로 들어온다.
  2. 로드밸런서에서 ASG라고 부르는 오토스케일링 그룹으로 부하를 분산시키게 된다.
  3. 오토스케일링 그룹은 아마존 머신 이미지를 필요로 하며 클라우드워치라는 클라우드 모니터링 서비스를 사용해서 서버의 용량을 늘릴지 줄일지 결정하게 된다.

### 2. EC2 인스턴스 생성하기 (서울 리전, Bitnami Wordpress, t2.micro)

<img width="1764" alt="AutoScaling-1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/cec92be5-efaa-456e-884e-7efcbe939066">

### 3. ALB 생성하기 (EC2 인스턴스와 같은 리전)

<img width="1760" alt="AutoScaling-2 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/2836b7be-d474-48dd-9c2d-675a0c182e95">

<img width="1769" alt="AutoScaling-2 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/22f44ce0-5f85-4af6-b2c2-1fb8c2ead637">

### 4. 생성한 EC2 인스턴스를 기반으로 AMI 생성하기

<img width="1767" alt="AutoScaling-3" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/e8f9dccb-4eda-4467-b92e-fd813a6b8235">

### 5. Auto Scaling Group(ASG) 만들기
- 시작 템플릿도 함께 생성하기
- ALB와 연결하기

<img width="1776" alt="AutoScaling-4 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/8f30a39d-6563-41d1-9b0e-0c33802d3914">

<img width="1769" alt="AutoScaling-4 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/d12fdf22-b349-4862-ad2a-158dab986136">

### 6. EC2 인스턴스에 ssh 로 접속하고 stress를 사용하여 Auto Scaling 작동 테스트 하기

<img width="1762" alt="AutoScaling-5 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/3513f9b6-8940-4bb1-a8cf-adf37bed33c7">

<img width="837" alt="AutoScaling-5 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/64b36004-2d55-4b6e-a309-62f46115e957">

<img width="1864" alt="AutoScaling-5 3" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/579be20d-7226-4972-a496-6cf9b1a5b30d">

### 7. 모든 리소스(EC2, AMI, ASG, ALB 등) 정리하기

<img width="1714" alt="AutoScaling-6 1" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/11ee9f5e-0f92-4f29-bf08-6cd837dd302d">

<img width="1714" alt="AutoScaling-6 2" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/1e3c6b53-d7d7-4530-b34c-db9a38553898">

<img width="1716" alt="AutoScaling-6 3" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/72380e22-435e-4ed2-8e8d-ae04002ae617">

<img width="1716" alt="AutoScaling-6 4" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/9bc359af-da4c-40df-b8fc-9c6ea7e46fe7">

<img width="1713" alt="AutoScaling-6 5" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/7551e320-9386-42c4-8275-0753026f6553">

<img width="1713" alt="AutoScaling-6 6" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/b386dd8c-a4a1-4c16-9b15-abcdf56af274">

<img width="1714" alt="AutoScaling-6 7" src="https://github.com/Hjoowhi/AWS-Assignment/assets/157435520/c2439497-c1a3-42ba-8a27-6948d3eee7b8">
