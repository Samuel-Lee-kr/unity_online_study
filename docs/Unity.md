# 유니티 내용 정리

## 1. Rigidbody2D

Rigidbody2D는 오브젝트를 물리엔진이 제어하게 만듦  
2D 에서는 오브젝트가 XY 평면에서만 움직이고, 그 평면에 수직인 축을 중심으로만 회전

Collider2D 컴포넌트는 Rigidbody2D 에 암시적으로 연결됨  

#### Body Type
* Dynamic - 모든 프로퍼티 사용 가능 & 중력과 힘의 영향
* Kinematic - 매우 정확한 사용자 제어 하에 움직임, 중력과 힘의 영향이 없음
* Static - 전혀 움직이 않도록 디자인, 움직일 수 없는 오브젝트처럼 동작

## 2. Collider2D
2D 충돌체의 모양을 정의하며, 게임 오브젝트 간 상호작용을 위해 사용

#### Collider List
* BoxCollider2D
* CircleCollider2D
* PolygonCollider2D
* EdgeCollider2D
* CapsuleCollider2D
* CompositeCollider2D

#### 중요 메시지
* OnCollisionEnter2D - 현재 오브젝트와 다른 오브젝트가 닿을 때 호출되는 메소드
* OnCollisionStay2D - 현재 오브젝트와 다른 오브젝트가 닿아있을 때 호출되는 메소드
* OnCollisionExit2D - 현재 오브젝트와 다른 오브젝트가 떨어질 때 호출되는 메소드

## 3. MonoBehaviour
유니티의 모든 스크립트가 파생되는 기본 클래스

### public 함수 중 유용한 함수
* Invoke - 메소드 이름을 호출
* CancelInvoke - 모든 Invoke 정지
* StartCoroutine - 입력 인자인 String OR IEnumerator 를 시작
* StopCoroutine - 입력 인자인 String OR IEnumerator 를 정지
* StopAllCoroutine - 모든 코루틴을 정지
* GetComponent - 해당 제네릭 타입의 object를 반환

### 중요 메시지
* Awake - 인스턴스가 로딩될 때 호출되는 메소드
* OnCollisionEnter2D - 현재 오브젝트와 다른 오브젝트가 닿을 때 호출되는 메소드
* OnCollisionStay2D - 현재 오브젝트와 다른 오브젝트가 닿아있을 때 호출되는 메소드
* OnCollisionExit2D - 현재 오브젝트와 다른 오브젝트가 떨어질 때 호출되는 메소드
* OnDestroy - MonoBehaviour가 없어질 때 호출되는 메소드
* OnDisable - inactive 혹은 disabled() 될 때 호출되는 메소드
* OnEnable - active 혹은 enable() 될 때 호출되는 메소드
* OnMouseDown - 마우스를 눌렀을 때 호출되는 메소드
* OnMouseDrag - 마우스를 계속 누르고 있을 때 호출되는 메소드
* OnMouseEnter - 마우스가 Collider 안쪽으로 들어왔을 때 호출되는 메소드
* OnMouseExit - 마우스가 Collider 바깥으로 나갔을 때 호출되는 메소드
* OnMouseOver - 마우스가 Collider 에 있을 때 지속 호출되는 메소드
* OnMouseUp - 마우스 클릭을 뗐을 때 호출되는 메소드

### 주요 변수
* enable
* gameObject
* tag
* transform
* name