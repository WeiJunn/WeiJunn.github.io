---
title: Hello Vue
date: 2021-05-19 09:33:39
tags: Vue
categories: Vue
---
# 用Vue实现点击按钮加一减一

Html

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="index.css">
    <title>Document</title>
</head>
<body>
    <div id="hello-vue">
        <h1>当前数为:{{counter}}</h1>
        <button @click="add">+</button>
        <button @click="sub">-</button>
    </div>
</body>
    <script src="https://unpkg.com/vue@next"></script>
    <script src="mian.js"></script>
</html>
```
css 有点难看

```css
*{
    margin: 0;
    padding: 0;
    color: white;
}
html,body{
    box-sizing: border-box;
    scroll-behavior:smooth;
}
#hello-vue{
    font-size: 50px;    
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100vh;
    background-image: linear-gradient(62deg, #3a3d40 0%, #181719 100%);
}
button{
    width: 10%;
    height: 3%;
    color: teal;
    margin-top: 20px;  
    transition: all 0.5s linear;
}
button:hover{
    transform: scale(1.2);
    border-radius: 4px; 
}
```

Javascript

```javascript
const app = {
    data() {
      return {
        counter: 0,
         }
      },
      methods:{
        add: function(){
            console.log('加一');
            this.counter++;
        },
        sub: function(){
            console.log('减一');
            this.counter--;
        }
      }
    }
  Vue.createApp(app).mount('#hello-vue')
//把app绑定到id为hellow-vue的控件上
```

运行效果:<a href="https://weijunn.github.io/Vue/" target="_blank">Vue</a>