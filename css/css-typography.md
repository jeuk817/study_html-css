### text-align
```html
<style>
    p{
      text-align: justify; /* 양쪽정렬 */
      border:1px solid gray;
    }
</style>
```

### font
```html
<style>
  #id1{
    font-size:5rem;
    font-family: arial, verdana, "Helvetica Neue", sans-serif; /* 앞에 글자스타일이 없으면 뒤에거가 실행, sans가 붙으면 장식이 안달리 글자, 없으면 장식이 달린 글자 */
    font-weight: bold; /* 글자 굵기 */
    line-height: 2; /* 글간격 */
  }
  #id2{
    font:bold 5rem/2 arial, verdana, "Helvetica Neue", sans-serif; /* 한번에 붙여서 쓸대 font를 사용한다. 순서를 잘 지켜야한다. */
  }
</style>
```

### web font
```html
<head>
    <link href="https://fonts.googleapis.com/css?family=Indie+Flower|Londrina+Outline|Open+Sans+Condensed:300" rel="stylesheet"> 
    <style>
      #font1{
        font-family: 'Open Sans Condensed', sans-serif;
      }
      #font2{
        font-family: 'Indie Flower', cursive;
      }
    </style>
</head>
<body>
    <p id="font1">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce facilisis lacus eu ex rhoncus pretium. Sed vestibulum risus pharetra, consequat nibh ac, ornare nunc. Nunc eu dui eget lorem aliquet finibus.
    </p>
    <p id="font2">
      Quisque nec arcu felis. Vestibulum gravida, augue eu facilisis tempus, neque erat tincidunt nunc, consequat ultrices felis urna eu augue. Nulla ut urna purus. Curabitur ultricies rutrum orci malesuada tempor.
    </p>
</body>
```