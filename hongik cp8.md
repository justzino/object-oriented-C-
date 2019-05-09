  * <표현>
  * base class / derived class 
  * base class로부터 상속받은 derived class
  * 혹은 derived class는 base class의 member function을 상속 받았다.

  * 상속관계에 있는 클래스들간의 생성자 실행과 소멸자 실행 순서.
  * 묵시적으로 base class constructor 선택
    + derived class 가 생성이 될때 base class의 default 생성자가 이용이 되는데, 이때
    + base class에 default 생성자가 없으면(다른 생성자만 만들어져있으면) 컴파일 오류가 발생한다.
  * 명시적으로 base class constructor 선택
  * 
  * 아래 코드의 생성자를 주목.
  
<code>

	class NamedCircle :public Circle
	{
		string name;
	public:
		NamedCircle(int radius, string name) :Circle(radius);
		void show();
	};

</code>

  * 실행시 'expected {' 라고 error 발생
    
<code>

	NamedCircle(int radius, string name) :Circle(radius) {}

</code>

  * 위와 같이 변경하면 해당 'function already has a body'라는 error 발생
  * 즉, derived class의 constructor을 declare할때 base class의 constructor을 이용하는 경우 아래 코드와 같이
  
<code>
	
	NamedCircle(int radius, string name);	// derived class내에 declaration 부분
	

	
	NamedCircle::NamedCircle(int radius, string name) : Circle(radius)	// 구현 부분
	{}

</code>


  * 업캐스팅과 다운캐스팅의 차이도 알아둘 것: 다운캐스팅의 경우 강제 타입 변환 반드시 필요!!!
  
