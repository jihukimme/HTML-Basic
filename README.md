# HTML-CSS-Basic
This is basic of HTML and CSS.
<img
      width="400px"
      src="https://images.velog.io/images/jqdjhy/post/c1225a25-b178-4ece-9af6-926e876195d1/HTML&CSS.png"
    />

* * *

# HTML
구글, 유튜브 ... 등등의 웹페이지에서 보는 모든 디자인적인 부분들은 HTML, CSS로 이루어졌다고 생각하면 된다.  
웹페이지의 페이지 소스 = HTML + CSS  
HTML과 CSS를 통해서 웹페이지를 만들 수 있다.  
HTML의 형식은 처음에는 문서의 형태로 만들어졌다.  

## 기본적인 html:5 형식  
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

## HTML의 태그
<태그이름>컨텐츠</태그이름>으로 끝나는 부분을 HTML Element라고 한다.  
ex: ```<h1>My First Heading</h1>```  
HTML은 이러한 Element들의 조합이다.  
다양한 Element들이 있다.  


## HTML 자주 쓰이는 element
```
<input type="text" />
<input type="number" />
```

선택 버튼  
```
<select class="select-style">
      <option>Seoul</option>
      <option>Jeju</option>
</select>
```  
테이블 만들기  
```
<table>
      <thead class="tb-head">
        <tr>
          <td>이름</td>
          <td>지역</td>
          <td>전화번호</td>
        </tr>
      </thead>
      <tbody class="tb-body">
        <tr>
          <td>김지후</td>
          <td>대구광역시</td>
          <td>010-4109-2237</td>
        </tr>
      </tbody>
</table>
```

네이버의 하이퍼링크 달기 . . ```target="_blank"```를 통해서 새로운 창을 통해 네이버 접속    
```<a href="https://www.naver.com" target="_blank">네이버</a>```  


## HTML의 Attribute
```
<img
      width="400px"
      src="https://images.velog.io/images/jqdjhy/post/c1225a25-b178-4ece-9af6-926e876195d1/HTML&CSS.png"
    />
```  
위의 Element에서 width와 src처럼 HTML Element의 추가적인 속성을 관리하기 위한 요소이다.   
각각의 Element마다 서로 다르고 다양한 Attribute이 있다.  

```
<p style="color: red">My First Paragraph</p>
```
위의 style은 Element에 디자인을 입히는 Attribute이다.  

```
<p style="color: red">I am red</p>
<p style="color: blue">I am blue</p>
<p style="font-size: 30px">I am big</p>
```  
위와 같은 예를 들 수 있다.


* * *


# CSS
CSS를 통해서 전체 페이지 Element에 디자인을 한번에 쉽게 적용한다.  
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <style>
      .color-primary {
        color: red;
      }

      .font-50 {
        font-size: 50px;
      }
    </style>
  </head>
  <body>
    <h1>My First Heading</h1>
    <p class="color-primary font-50">I am red</p>
    <p style="color: blue">I am blue</p>
    <p class="color-primary" style="font-size: 30px">I am big</p>

    <img
      width="400px"
      src="https://images.velog.io/images/jqdjhy/post/c1225a25-b178-4ece-9af6-926e876195d1/HTML&CSS.png"
    />
  </body>
</html>
```  
위의 코드에서 ```<head>```태그 안의  
```
<style>
      .color-primary {
        color: red;
      }

      .font-50 {
        font-size: 50px;
      }
    </style>
```
안에 있는 .color-primary와 .font-50을 클래스라고 한다.   
편의를 위해 클래스를 만들어 스타일을 지정하게 되는데..  
이를 css파일로 만들어서 사용하게 된다. (CSS - 디자인을 통합적으로 관리하는 역할)   


style.css 파일 사용하기  
```
.color-primary {
  color: red;
}

.font-50 {
  font-size: 50px;
}
```
를 style.css 파일에 입력을 했다.  
이를 html에서 사용하기 위해서  

```<head>```태그 안에  
```
 <link rel="stylesheet" href="style.css" /> 
```  
```<link>```태그를 추가해 style.css와 연결시킨다.   



## CSS의 선택자  
```
선택자 { 
    color: red;
    padding: 5px;
    속성: 속성값;
    선언;
}

전체 선택자
* {

}

태그 선택자
p {

}

클래스 선택자
.class1 {

}

id 선택자   
#id1 {
  background: yellow;
  color: darkgreen;
}

자식 선택자
.tb-head > tr > td {
  border: 1px solid #000;
  font-size: 14px;
  font-weight: bold;
  color: red;
}

.tb-body > tr > td {
  border: 1px solid #000;
  font-size: 14px;
  font-weight: bold;
}

하위 선택자
.tb td {
  border: 1px solid #000;
}
```


## Event란?  
event - 클릭, 스크롤 .. 등등의 동작  
```<body>```태그 안에  
```
<button type="button" onclick="javascript: alert('click button!!');">Click</button>
```  
Click이라는 텍스트를 갖는 button 생성  
클릭시 click button!!이라는 텍스트를 표시하는 이벤트 발생.  


