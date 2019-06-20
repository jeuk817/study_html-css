### 인라인 블럭레벨
```html
<style>
 h1,a{
     border: 1px solid red;
 }
 h1{
     display: inline; /* 자신의 영역만 잡아먹는다 */
 }
 a{
     display: block; /* 자신을 포함한 블럭전체의 영역을 잡아먹는다. */
 }
</style>
```
- solid = 단선
- dotted = 점선

### 박스모델
```html
<style>
    p{
        border: 10px solid red;
        padding: 20px; /* 박스의 선과 본문간의 간격(박스 안) */
        margin: 40px; /* 박스선 바깥의 공간, 다른박스 또는 다른 요소와의 간격(박스 밖) */
        width: 100px; /* 박스의 폭을 강제로 조정. !!하지만 인라인방식에서는 폭과 높이가 무시된다.!! */

    }
</style>
```

### box-sizing
```html
<style>
    *{
        box-sizing: border-box; /* 원래는 테두리는 무시하고 안에있는 콘텐츠의 크기를 기준으로 width,height가 지정됬지만 이렇게 설정해두면 테두리를 포함한 크기로 지정된다. */
    }
    div{
        margin: 10px;
        width: 150px;
    }
    #small{
        border: 10px solid black;
    }
    #large{
        border: 30px solid black;
    }
</style>
```

### 포지션
```html
<style>
    html{border:1px solid gray;}
    div{
        border: 5px solid tomato;
        margin: 10px;
    }
    #me{
        position: relative;
        /* 기본값은 static으로 설정되어있어서 그 위치를 벗어나지못한다. relative로 지정하면 부모를 기준으로 움직일 수 있다. absolute는 html전체를 기준 혹은 relative로 지정된 부모를 기준으로 움직인다.*/
        left: 100px;
        top: 100px;
    }
</style>
<div id="other">other</div>
<div id="parent">
    parent
    <div id="me">me</div>
</div>
```

- position :    relative = 부모를 기준으로 움직일 수 있다.  
                absolute = 부모중 위치가 정해지지 않은 부모(relative)를 기준으로 움직인다.(없다면 html전체를 기준으로)  
                fixed = 화면의 특정위치에 고정시켜서 스크롤과는 상관없이 움직이지 않도록 설정한다.  

### flex
```html
<style>
    .container{
        background-color: powderblue;
        height: 200px;
        display: flex; /* 플레스로 쓸 부모에게 display값으로 flex를 준다. */
        flex-direction: row; /* 기본값 row, 반대로 정렬 row-reverse, 열 column, column-reverse */
    }
    .item{
        background-color: tomato;
        color: white;
        border: 1px solid white;
    }
</style>
<div class="container">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
    <div class="item">5</div>
</div>
```

```html
<style>
    .container{
        background-color: powderblue;
        height: 200px;
        display: flex; 
        flex-direction: row; 
    }
    .item{
        background-color: tomato;
        color: white;
        border: 1px solid white;
        flex-grow: 1; /* 값 1을 주면 부모의 공간을 n빵한다. */
    }
    .item:nth-child(2){
        flex-grow: 2; /* 이 요소만 값을 더준다.(만약 위에 .item에 flex-grow를 없애면 이 한 요소가 나머지 부모의 공간을 다 차지한다. */
    }
</style>
<div class="container">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
    <div class="item">5</div>
</div>
```

```html
<style>
    .container{
        background-color: powderblue;
        height: 200px;
        display: flex; 
        flex-direction: row; 
    }
    .item{
        background-color: tomato;
        color: white;
        border: 1px solid white;
    }
    .item:nth-child(2){
        flex-basis: 300px; /* 화면의 크기를 줄이면 이 요소의 크기가 자동으로 화면에 맞춰 줄어든다. */
        flex-shrink: 0; /* 이 값이 0이면 화면이 줄어들더라도 이 요소의 크기는 줄어들지 않는다.(그냥 화면만 줄어들고 옆으로 이어진다.) 만약 이 값을 1로주면 다시 화면에 맞춰 줄어든다. */
    }
    .item:nth-child(1){
        flex-basis: 300px;
        flex-shrink: 2; /* flex-shrink의 값을 여러 요소에게 주면, 화면이 줄어들 때 이 값들을 전부 더한값에서 각 요소의 shrink값만큼 비율에 맞춰 줄어드는 속도가 달라진다. */
    }
</style>
<div class="container">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
    <div class="item">4</div>
    <div class="item">5</div>
</div>
```

### float
```html
<style>
    img{
        width:300px;
        float:left; /* 이 요소를 피해서 글이 적힌다. 이 요소는 왼쪽에 있다. right하면 오른쪽. */
        margin:20px;
    }
    p{
        border: 1px solid gray;
    }
</style>
<img src="">
<p>
    lorem asdnf;lh asdhiao a;nj ;nwfnv;f.....
</P>
<p style="clear:both;">
    lorem asdhfi hoai hnoivn ofnweof naw........
</p>
```

### flexbox froggy 플렉스 게임!!!!!
- justify-content : 양옆으로 움직인다.(모든아이템을 움직인다.)
    - justify-content: flex-start, flex-end, center, space-between(요소들 사이에 동일한 간격), space-around(요소들 주위에 동일한 간격)

- align-items : 아래위로 움직인다.(모든아이템을 움직인다.)
    - align-items: flex-start, flex-end, center, baseline(요소들을 컨테이너의 시작위치에 정렬합니다.), stretch(요소들을 컨테이너에 맞도록 늘립니다.)

- align-self : 해당 아이템만 움직인다.

- flex-direction : 플렉스 컨테이너 내의 아이템들을 배치할때 쓴다.
    - flex-direction: row(기본값), row-reverse(이때 시작과 끝점도 달라진다. justify-content: flex-end를 해야지 아이템들이 왼쪽으로 간다.), column, column-reverse(가로세로가 바뀐다. 아이템들을 아래로 내리려면 justify-content: flex-end를 해줘야한다.)

- order : 플렉스 컨테이너 안에서 현재 아이템의 배치 순서를 지정한다.
     - order: 3; <!--컨테이너 내의 아이템 순서는 오름차순이고, 같은 값일 경우 소스 코드의 순서대로 정렬된다. 이때 order로 번호를 주어 해당 위치로 이동시킬수 있다. -->

- flex-wrap : 아이템들을 강제로 한줄에 배치할것인지, 아니면 가능한 영역 내에서 벗어나지 않고 여러행으로 나누어 배치할 것인지 결정한다.
    - flex-wrap: nowrap, wrap, wrap-reverse;

- flex-flow : flex-direction과 flex-wrap 속성을 합친것이다.
    - flex-flow: row wrap, row-reverse nowrap, column wrap-reverse, column wrap;

- align-content : 아이템들을 줄단위로 아래, 위로 움직인다.(flex-wrap: nowrap;이면 의미가 없다.)
    - align-content: start, center, space-between, space-around;

