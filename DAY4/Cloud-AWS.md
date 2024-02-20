# 클라우드, AWS

### ☑︎ 클라우드 컴퓨팅 개념 설명해보기

➡️ 클라우드 컴퓨팅(Cloud Computing)의 다양한 정의

- 데이터 저장과 접근을 인터넷으로 언제 어디서든 접근 가능한 기술

- 바로 사용 가능하고 사용한 만큼만 과금되는 전산 기반 시설들 (Infra Structure)

- 전산 하드웨어 장비들의 가상화(Virtualization) 기술

➡️ **클라우드 컴퓨팅이란**  
서버, 스토리지, 네트워크 같은 물리 하드웨어 장비 뿐만 아니라, 플랫폼과 애플리케이션이라는 소프트웨어까지 포함하는 개념인 전산자원들을 공유하는 기술과 도구의 집합으로, 서버 스토리지 같은 물리 하드웨어 장비와 어플리케이션 같은 소프트웨어까지 포함하는 전산 자원들을 인터넷을 통해 공유해서 사용할 수 있게 해주는 것이다.

---

### ☑︎ 리전, 가용 영역, 엣지 로케이션 개념 설명해보기

- **리전(Region)** : AWS의 서비스들가 운영되는 지역으로 복수 개의 데이터 센터들의 집합으로, 쉽게 말해 AWS의 서비스들이 제공되는 서버의 물리적인 국가/도시 단위의 위치를 말한다.

- **가용 영역(AZ, Availability Zones)** : 리전 내에 위치한 복수 개의 데이터 센터들로, 물리적으로 분리되어 있어 고가용성/이중화 구성의 기본 요소가 된다.

- **엣지 로케이션(Edge Location)** : CloudFront 같은 엣지 서비스의 캐시 서버가 운영되는 데이터 센터로, AWS의 CDN 또는 CDS의 여러 서비스들을 가장 빠른 속도로 제공(캐싱)하기 위한 거점이라 할 수 있다.

---

### ☑︎ 클라우드의 종류 설명해보기 (힌트. 피자를 먹는 네 가지 방법)

#### 피자를 먹는 네 가지 방법

- 홈 피자(Made at home) : 반죽을 만드는 것을 포함한 모든 재료를 직접 구매하여 집에서 피자를 만들 수 있습니다.  
  (You can make a pizza at home where you’re responsible for buying all of the ingredients including making the dough.)

- 냉동 피자(Take & Bake) : 재료 중 일부와 미리 포장된 반죽을 구매할 수 있습니다.  
  (You can purchase some of the ingredients and buy pre-packaged dough.)

- 배달 피자(Pizza Delivered) : 집에서 피자를 배달시켜 먹을 수 있습니다.  
  (You can have pizza delivered to your home.)

- 음식점 피자(Dined Out) : 간단하게 현지 식당에 피자를 먹으러 갈 수 있습니다.  
  (You can simply load up the family and head out for pizza at your local dining establishment.)

위의 어떤 경우라도 피자를 먹고 있지만 내가 일을 하느냐, 다른 사람이 나를 위해 일을 하느냐에 차이가 있다.  
위 예시를 서버에 빗대어 본다면 

#### ✅ Traditional On-Premises
- 홈 피자  
  : 집에서 컴퓨터를 직접 사서 설치하고 사용하는 경우, 클라우드를 사용하지 않고 그냥 자신의 집에 있는 컴퓨터만 사용하면 된다.  
  : 서버, 네트워크, OS, 소프트웨어까지 전부 다 직접 관리해야 한다.

#### ✅ Infrastructure as a Service (IaaS)
- 냉동 피자  
  : 인프라 스트럭처만 대여하는 경우, 돈을 내고 인프라 스트럭처를 대여해서 사용한다.  
  : 서버, 스토리지, 네크워크 등의 장비만 돈을 내고 대여하고, 운영체제와 미드웨어 등의 설치는 직접 해야 한다.

#### ✅ Platfrom as a Service (Paas)
- 배달 피자  
  : 플랫폼까지 대여하는 경우, 돈을 내고 인프라 스트럭처와 같이 플랫폼까지 대여해서 사용한다.  
  : 운영체제가 설치된 상태로 빌리는 것으로, 바로 소프트웨어를 설치한 후 사용하면 된다.

#### ✅ Software as a Service (SaaS)
- 외식 피자  
  : 소프트웨어까지 모든 것을 다 대여하는 경우로, 그냥 바로 사용하면 된다.
