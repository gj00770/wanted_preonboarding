# 프리온보딩

node version 15.14.0 에서 작업했습니다.

## toggle
 
### 구현한방법
토글컨테이너를 만들어줍니다 이때 토글을 클릭하면 좌우로 움직이는것이아닌 선택메뉴로 움직이기 때문에 onclick event가 두개필요하다고 생각했습니다. 그래서 만약 왼쪽 메뉴를 클릭하면 토글박스의 transform의 translateX 를 0px을주고 아니면 토글컨테이너의 절반만큼 이동시키는 방법 으로 구현하였습니다.

### 구현한이유
처음에 ref로 토글박스에 접근해서 토글을 이동시켜줄려고했지만 ref를 사용하는것은 지양되기때문에 이러한 방식으로 구현하였습니다.


### 어려웠던이유
처음에 Ref로 접근할려다가 Ref를 사용하는것은 최대한 지양해야되기때문에 다른방법이 무슨방법이 최선의 방법인지 생각하는게 어려웠습니다.


## tab

### 구현한방법
toggle과 같은 방식으로 슬라이드 애니메이션을 구현하였습니다. onclick 이벤트로 클릭한 메뉴의 정보를 state 에담고 그정보를 토대로 슬라이드 에니메이션을 변화시키면서 탭에 컬러를 변화시켰습니다

### 구현한이유
처음에 ref로 토글박스에 접근해서 토글을 이동시켜줄려고했지만 ref를 사용하는것은 지양되기때문에 이러한 방식으로 구현하였습니다.

### 어려웠던이유
처음에 Ref로 접근할려다가 Ref를 사용하는것은 최대한 지양해야되기때문에 다른방법이 무슨방법이 최선의 방법인지 생각하는게 어려웠습니다.

## slider

### 구현한방법
slider컨테이너를만들고 그안에 퍼센트를 나타낼 슬라이더 바디를 넣어주고 토글과. 바디안에는 25% 50% 를 위치를 나타내줄 작은 원들을 일정한간격으로 만들어주고 토글원이 이동시 색이변하게 만들기위해 작은바를 만들어줍니다.  그후 ref로 toggle해줄원과 슬라이더 바디를 선언해줍니다. 슬라이더 바디의 pagex의 좌표를 마우스의 위치와 비교해서 토글을 움직이는 방법으로 구현했습니다. 여기서 click event는 마우스가 다운될시 addeventlistener로 mousemove와 mouseup 이발생되고 mousemove이벤트에서는 마우스의 x좌표와 pageX의 좌표를 비교해서 작은원을 움직이면서 바를 이동시켜줍니다. 그리고 나서는 mouseup이벤트가 발생했을 시에는 removeEventLister로 두개의 addeventlistener들을 종료 시켜줍니다. 그리고 퍼센트를 클릭할시 onclick 이벤트를만들어서 각각 0% 25% 50% 75% 100% 구역에 알맞은 X값을넣어주었습니다.

### 구현한이유
ref로 pageX의 좌표를 구한이유는 창의 크기가 불규칙하기때문에 그때그때 X좌표를 구해서 움직이게 하였습니다. 
그리고 창을 작거나 크게하면 토글의 위치를 고정시키기위해 토글의 position은 absolute가아닌 위치가 부모의 요소에 영향을받는 relative로 설정하였습니다
슬라이더 바디를 따로 만들어준이유는 작은원들과 움직일 토글의 중심을 맞추기위해서입니다.

### 어려웠던이유
 좌표를 받아와서  구현해야되는지 원의 중심을 잡아주는 식을 만드는게 어려웠습니다.

## input

### 구현한방법
일단 이메일 폼형식대로 html레이아웃을잡은다음에 이메일에 onChange이벤트를 걸어서 input 태그에 value값이 변할때마다 정규 표현식을사용하여서 validation체크를 하게만들었습니다.만약 validation아 true값이 나오면 input 태그안에 있는 아이콘의 색상을 변경해줍니다 그리고 input태그안에 onblur 이벤트를 걸어서 만약 input태그 가 아웃포커싱될때 이메일이 폼이 적절하지않다는메세지를 화면에 보여지게합니다.

비밀번호칸안에는 눈모양 아이콘을넣어주어서 비밀번호 input 태그안에 type속성을 text로 바꿔주고 다시 클릭했을시 type속성을 password로 바꿔줍니다.

### 구현한이유
이메일폼 validation 체크를 하기위해서 정규표현식을 상요하는게 효율적이라고 생각했습니다.
### 어려웠던이유
input태그안에 아이콘을 넣는게 어려웠습니다.

## dropDown


### 구현한방법


### 구현한이유


### 어려웠던이유
