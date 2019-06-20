### 선택자
```html
<style>
    li {
        color:red;
        text-decoration:underline;
    }
    #select {
        font-size:50px;
    }
    .deactive{
        text-decoration: line-through;
    }
</style>
<h1 class="deactive">수업의 순서</h1>
<ul>
    <li class="deactive">HTML</li>
    <li id="select">CSS</li>
    <li class="deactive">JavaScript</li>
</ul>
```

- id:#id = 아이디는 하나를 대상으로할때 쓴다.
- class:.class = 클래스는 여러대상을 상대로 쓴다.

### 부모자식 선택자
```html
<style>
    ul li{
      color:red;
    }
    #lecture>li{
      border:1px solid red;
    }
    ul,ol{
      background-color: powderblue;
    }
</style>

<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ul>
<ol id="lecture">
    <li>HTML</li>
    <li>CSS
        <ol>
          <li>selector</li>
          <li>declaration</li>
        </ol>
    </li>
    <li>JavaScript</li>
</ol>
```

- ul li: 띄어쓰기 = 부모 자손 선택자 = 부모 밑에있는 모든 선택자를 바꿈
- #lecture>li: 꺽쇠 = 부모 자식 선택자 = 부모 바로밑에있는 선택자만 바꿈
- ul,ol: 쉼표 = 동반 선택자 = 둘다 같이 바꿈

### 가상 클래스 선택자
```html
<style>
    a:link{
        color:black; /* 방문안한 링크*/
    }
    a:visited{
        color: red; /* 방문한 링크*/
    }
    a:hover{
        color:yellow; /* 마우스가 위로 올라왔을때 */
    }
    a:active{
        color:green; /* 마우스클릭한 상태(드래그) */
    }
    a:focus{
        color:white; /* 포커스된 상태 */
    }
</style>
```

