# Movie-Website

## 📅  22.07.02 ~ 22.07.03

### ✅  프로젝트 및 파일 생성

### ✅  css 파일 연결, 구글폰트 세팅 및 cdn 연결

### ✅  navbar, sidebar, section 기본 배치

- 레이아웃 고려해서 시맨틱 태그로 사용 : nav, section
- 스크롤링 제거, 사이드바 상단 고정 : position: fixed / top: 0 (overflow: hidden 도 활용 가능)
- 사이드바 아이콘 간격
    1. padding-top 으로 전체적으로 상단에서 얼마나 거리두고 배치할지 설정
    2. 세로 배치된 아이콘 간격은 margin-bottom 으로 조정
- 메인 contents section 부분 container 위치 세팅
    1. 세부적인 위치 조정 : height
- vh, vw, width, height % 차이
    - width, height % : 부모의 영향을 받아서 적용됨
    - vh, vw : 사용하는 기기의 스크린 범위에 영향 (스크롤 부분까지 포함됨)
    - 참조 : [https://shinye0213.tistory.com/372](https://shinye0213.tistory.com/372)

###  ✅  내부 엘리먼트 배치 및 적용

- 같은 범주의 요소중 다른 속성을 적용해야할 때
    - id 를 부여하거나 nth child 적용하는 방식을 생각했었음 ⇒ 그냥 적절한 class 이름을 하나 더 붙여주고 CSS 선택자로 클래스 이름을 붙여서 적용(good!)
    
    ```css
    .menu-list-item.active {  /* class 를 2개 부여해서 선택해 줌 */
        font-weight: bold;
    }
    ```
    
- nav 하위 영역별 container 세분화 (logo, menu, profile) ⇒ 요소를 배치할 때도 container를 만들어 주고 넣어야 배치 조절이 용이한듯 함
- toggle (dark or light)
    - toggle ball 요소 독립적이고 자유롭게 움직이게 하기 (겹치게 하기위해) ⇒ 해당 요소에 position : absolute;
    - 부모 요소 내부 안에서만 움직이게 하기 ⇒ 부모에 position : relative;
- object-fit : 삽입한 이미지 요소를 가로세로 비율 유지하면서 컨테이너에 꽉 차게 설정
- linear-gradient : 이미지에 그라디언트 구현

```css
.featured-content {
    height: 50vh;
    background-image: linear-gradient(to bottom, rgba(0,0,0,0), #151515), url('./img/f-1.jpg');
}
```

### ✅  fontawesome  free 아이콘 활용 (cdn 방식으로 가져옴)