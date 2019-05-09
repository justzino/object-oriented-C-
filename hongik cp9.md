  * 각각의 포인터의 함수 호출시 어떤 class(base, derived)를 호출하는가
   
<code>
    
      Derived d, *pDer;
      pDer = &d;
      pDer->f(); // Derived::f() 호출
      Base* pBase;
      pBase = pDer; // 업캐스팅
      pBase->f(); // Base::f() 호출
    
</code>

  * 가상 함수를 재정의하는 것을 '오버라이딩'으로, 그렇지 않는 경우를 '함수 재정의'
  * 실행시에 할당이 결정(?)
