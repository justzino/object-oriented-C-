   * 각각의 포인터의 함수 호출시 어떤 class(base, derived)를 호출하는가
   
    <code>
    
      Derived d, *pDer;
      pDer = &d;
      pDer->f(); // Derived::f() 호출
      Base* pBase;
      pBase = pDer; // 업캐스팅
      pBase->f(); // Base::f() 호출
    
    </code>
