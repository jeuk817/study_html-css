### 캐스캐이팅 Cascading
```html
<style>
    li{color:red;}
    #idsel{color:blue;}
    #idsel{color:yellow;}
    .classsel{color:green;}
</style>
<ul>
    <li>html</li>
    <li id="idsel" class="classsel" style="powderblue">css</li>  <!-- 여기가 가장 우선순위가 높다. -->
    <li>javascript</li>
</ul>
<ol>
    <li>style attribute</li>
    <li>id selector</li>
    <li>class selector</li>
    <li>tag selector</li>
</ol>
```

- 우선순위: !important > style속성 > id > class > li 등...
