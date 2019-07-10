# CSS 속성에 관한것

### display: none과 visibility: hidden의 차이
- display: none은 자신의 영역을 차지하지 않는다.
- visibility: hidden은 자신의 영역을 차지한다. 그래서 차라리 opacity: 0; 이 더 낫다. 왜냐하면 이것은 GPU를 사용하기 때문에 rendering이 더 빠르다.
