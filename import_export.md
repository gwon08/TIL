# import / export

 

# import/export

> 변수나 함수, 자료형을 다른 파일로 저장해둔 뒤, 불러오는 방법이다.
> 
1. data.js(원하는 데이터파일)을 export(내보내다)하고
2. App.js.(불러와서 적용할파일)에 import(들여오다)

---

# export

## 1) data.js에서 App.js로 데이터를 내보낼 때

```jsx
// (data.js)
// var 변수명작명 = '데이터';
var dataName = 'react';
export default dataName;
```

1. 변수명, 함수명, 자료형 전부 내보낼 수 있다.                                           
2. 파일마다 export default라는 키워드는 하나만 사용 할 수 있다.

## 2) 여러개의 변수를 내보내고 싶을 때

```jsx
// (data.js)
var dataName1 = 'react1';
const fruits = ['사과', '귤', '배'];
function hello(){
	console.log('hello');
}

export { dataName1, fruits, hello };

```

---

# import

## 1) data.js에서 app.js로 데이터를 가져와서 쓸 때

```jsx
// (App.js)
// import 변수명작명 from '가져올데이터파일경로';
import Data from './data.js';
```

1. ‘./’은 현재경로를 뜻한다.
2. 변수명작명 부분은 자유롭게 작명할 수 있다.

## 2) 여러개의 변수를 가져다 쓰고 싶을

```jsx
// (App.js)
import { dataName1, fruits, hello } from './data.js';
```

이 경우에는 변수명작명이 불가능하고 export 했던 변수명을 그대로 쓴다
