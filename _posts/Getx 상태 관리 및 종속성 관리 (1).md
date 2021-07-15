# Getx Reactive 상태 관리

- `GetxController` extend 불필요
- 초기화 시 `.obs`를 사용하면 Rx형으로 바뀐다
    - `RxInt`
    - `RxString`
    - `RxDouble`
    - `RxBool`
    - `RxList`
    - `Rx<Enum>`
    - `Rx<class>`
    - etc...
- 값 변경 메소드 구현 시 `update()` 불필요
- **값이 변경 될 때**마다 함수 호출
    - non-reactive에서는 값이 변경되지 않아도 함수 호출 됌
- `GetxController`을 extends할 때 lifecycle함수들 사용가능
    - `onInit()`
    - `onClosed()`
    - etc...
        - `ever()` => 매번 호출 
        - `once()` => 처음 한번만 호출
        - `debounce()` => 마지막 변경 후 delay시 호출 **검색 자판에 활용**
        - `interval()` => 변경되는 동안 주기적으로 호출

# Getx 종속성 관리 A. Dependency

1. `Get.put(dependency)`
    - 일반적인 의존성 주입 방법
    - binding에 BindingBuilder을 통해 루트에서 의존성 주입 가능
    
    
2. `Get.lazyPut(dependency)`
    - controller가 사용될 때 의존성 주입 됌
    
    
3. `Get.putAsync(dependency)`
    - 비동기적 의존성 주입
    
    
4. `Get.create(dependency)`
    - 매번 새로운 controller 선언

# Getx 종속성 관리 B. Binding

- GetPage에서 BindingBuilder을 통해 여러 바인딩을 할 수 있다(?)

# GetxController vs GetxService

- GetxContoller => `Get.put(dependency, permanent = true)`
- GetxService => `GetxController` 대신 `GetxService` 상속
    - Get.reset() => **모든 Controller** 초기화

출처 유튜브 [개발하는 남자](https://youtube.com/playlist?list=PLgRxBCVPaZ_3bPtdyE0Tj-w1CFX01bgUE) Getx편
