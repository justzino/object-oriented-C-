base class
derived class 

<표현>
base class로부터 상속받은 derived class
혹은 derived class는 base class의 member function을 상속 받았다.

  * 상속관계에 있는 클래스들간의 생성자 실행과 소멸자 실행 순서.
  * 묵시적으로 base class constructor 선택
    + derived class 가 생성이 될때 base class의 default 생성자가 이용이 되는데, 이때
    + base class에 default 생성자가 없으면(다른 생성자만 만들어져있으면) 컴파일 오류가 발생한다.
  * 명시적으로 base class constructor 선택
 
<code>

	class NamedCircle :public Circle
	{
		string name;
	public:
		NamedCircle(int radius, string name) :Circle(radius);
		void show();
	};

</code>
