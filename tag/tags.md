### 이미지 태그
```html
<img src="food.jpg" height="300" alt="음식이미지" title="음식이미지">
```
- alt = 대체 텍스트
- title = 이미지 위에 마우스 올릴시 텍스트로 표시(태그처럼)

### 테이블 태그
```html
<table border="2">
    <tr>
        <td>이름</td> <td>성별</td> <td>주소</td>
    </tr>
    <tr>
        <td>circus</td> <td>남</td> <td>서울</td>
    </tr>
</table>
```
- table = 테이블을 만들 구역
- tr = table row 테이블 행
- td = 테이블 한 칸(열?)

### 선택 태그
```html
<form action="">
    <h1>색상</h1>
    <select name="color">
        <option value="red">붉은색</option>
        <option value="black">검은색</option>
        <option value="blue">파란색</option>
    </select>
    <h1>색상2 (다중선택)</h1>
    <select name="color2" multiple>
        <option value="red">붉은색</option>
        <option value="black">검은색</option>
        <option value="blue">파란색</option>
    </select>
    <input type="submit">
</form>
```
- select = 콤보박스를 넣을 구역
- option = 하나의 선택지
- select 안의 multiple = 여러선택지를 고를수있는 속성(ctrl을 사용해서 여러개를 고를수 있다.)

```html
<form action="">
    <p>
        <h1>색상(단일선택)</h1>
        붉은색 : <input type="radio" name="color" value="red">
        검은색 : <input type="radio" name="color" value="black" checked>
        파란색 : <input type="radio" name="color" value="blue">
    </p>
    <p>
        <h1>색상(다중선택)</h1>
        95 : <input type="checkbox" name="size" value="95">
        100 : <input type="checkbox" name="size" value="100" checked>
        105 : <input type="checkbox" name="size" value="105" checked>
    </p>
    <input type="submit">
</form>
```

### 라벨 태그
```html
<form action="">
    <p>
        <label for="id_txt">text</label>:
        <input id="id_txt" type="text" name="id" value="default value">
    </P>
    <p>
        <label for="id_pwd">password :</label>
        <input id="id_pwd" type="password" name="pwd" value="default value">
    </P>
    <p>
        <label>textarea:
        <textarea rows="2">default value</textarea>
        </label>
    </P>
    <p>
        <label>
            <input type="checkbox" name="color" value="red">붉은색
        </label>
        <label for="color_blue">
            <input id="color_blue" type="checkbox" name="color" value="blue">파란색
        </label>
    </P>
</form>
```

### method: get방식 post방식
```html
<form action="" method="post">
    <input type="text" name="id">
    <input type="password" name="pwd">
    <input type="submit">
</form>
```

- get = get방식은 url에 입력값의 정보를 태워서보낸다.
- post = post는 url에 표시가 안돼고 숨겨서 보낸다. 99% 이방식으로 보낸다.

### 파일 업로드
```html
<form action="" method="POST" enctype="multipart/form-data">
    <input type="file" name="profile">
    <input type="submit">
</form>
```

파일을 담을때 쓰는 속성... 아직은 모른다.  

### meta 태그
```html
<meta charset="utf-8">
<meta name="description" content="생활코딩의 소개자료">
<meta name="author" content="egoing">
<meta http-equiv="refresh" content="30">
```

- meta = 웹페이지의 내용은아니지만 그 내용을, 그 웹페이지를 설명하는 태그다.
- refresh는 몇초마다 웹페이지를 리프레시하는 것

### 의미론적 태그 semantic 태그

- 웹페이지에서 통상 많이 사용하는 구조에 의미를 분명히 부여하기 위해서 의미론적 태그를 새롭게 정의해서 제공하고 있다.

### iframe 태그
```html
<iframe src="http://opentutorials.org"></iframe>
```

- 다른 웹페이지를 넣을 수 있다.