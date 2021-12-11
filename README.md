# Asteriod
- 우주를 주제로 한 다방향 슈팅 아케이드 게임으로, 1979년 11월 아타리에 의해 출시되었다. 플레이어는 소행성대에 들어선 우주선 한 대를 조종하며 주기적으로 비행접시에 의해 경유된다.
<img width="436" alt="스크린샷 2021-12-11 오후 4 21 28" src="https://user-images.githubusercontent.com/65120581/145668217-12cae8e2-0fee-4c2f-a554-1bbeed5bc019.png">


## Game

## 패턴의 구조 
<img width="693" alt="스크린샷 2021-12-11 오후 4 13 49" src="https://user-images.githubusercontent.com/65120581/145668062-3bb55b46-fd02-427c-b9fe-5c99576cee79.png">

- 패턴의 참여자
  - 생산자(creator) : 팩토리 메소드가 선언 및 정의되는 추상타입
  - 구체적 생산자(concrete creator) : 팩토리 메소드를 재정의하여 실제 객체를 생성하는 클래스
  - 제품(product) : 생성될 객체들의 추상 클래스 또는 interface
  - 구체적 제품 클래스(concrete product) : 실제 생성될 객체의 클래스


- 참여자간 협력
  - 생산자 클래스나 Interface는 객체의 생성을 하위 클래스에 위임함
  - 보통 역할의 이름과 달리 객체의 생성이 생산자의 핵심 역할이 아님
  - 구체적 생산자는 매번 객체를 생성해야 하는 것은 아니며, 객체 풀과 같이 다양한 생성 로직을 사용할 수 있음

- 생성될 asteroidFacotry의 종류가 같은 추상타입(제품 참여자)을 사용한다.
```java 
	private AsteroidFactory asteroidFactory 
//		= new AsteroidDiamondFactory();
//		= new AsteroidRectangleFactory();
		= new AsteroidPolygonFactory();
```
