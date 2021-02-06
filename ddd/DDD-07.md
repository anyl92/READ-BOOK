## 객체 설계시 고민해볼만 한 것

- 정의
- 책임
- 속성
- 연관 관계

## ENTITY

  ENTITY는 식별성과 연속성이 중요하다. 식별성이란 ENTITY을 구분할 수 있는 유일한 값을 가지고 있다는 것을 의미한다. 연속성은 객체의 생명주기 동안 객체가 일관되는 것을 의미한다.

  식별성은 유일한 값을 가지는 것만 의미하는 게 아니다. ENTITY의 개념을 나타낼 수 있어야 한다. 식별성을 효과적으로 정의하기 위해서는 도메인을 이해해야 한다. ENTITY가 많아지면 성능 문제가 생기고 모델에 혼란을 주므로 이 객체가 식별이 필요한지 충분한 고민이 필요하다.

  객체의 행위가 명확하고 예측 가능하다면 연속성이 보장된 것이다. 속성과 행위에 집중하는 것보다 객체의 개념에 집중해야 한다. 개념에 필요한 행위만 추가하고 행위에 필요한 속성만 추가한다. 그 밖의 객체는 연관 관계를 가진 객체로 분리한다.

## VALUE OBJECT

  VALUE OBJECT는 식별성을 갖지 않고 도메인의 서술적인 측면(속성)을 나타내는 객체다. 모델에 포함된 요소의 속성에만 관심이 있으면 VALUE OBJECT를 사용하면 된다.

  객체의 속성을 나타내는 VALUE OBJECT에 대한 오해 세 가지가 있다.

- VALUE OBJECT는 단순하지 않다. 복잡한 알고리즘이 포함될 수도 있다.
- VALUE OBJECT가 다른 여러 객체를 조합해서 만들어 질 수도 있다.
- VALUE OBJECT가 ENTITY를 포함할 수도 있다.

  VALUE OBJECT를 사용하는 방법에는 복사와 공유가 있다.

  복사는 아래와 같은 경우에 사용한다.

- 분산 시스템에서는 복사를 사용한다.
- 데이터베이스에서 성능 최적화가 필요할 경우 사용한다.

  공유는 아래 세가지 경우에 사용한다.

- 공간이 절약하거나 객체 수를 줄이는 것이 중요한 경우 사용한다. (FLYWEIGHT 패턴)
- 통신 부하가 낮은 경우 사용한다. (중앙 집중형 서버)
- 불변성이 엄격하게 지켜지는 경우 사용한다.