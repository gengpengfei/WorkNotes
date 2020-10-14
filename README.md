# WorkNotes
随手记
- css3动画实现放大水波纹
```
//-- 动画元素
#menu .focusable:focus::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border-radius: 100vw;
    opacity: 0;
}
#menu .menu.focusable::before {
    animation: menu-animate 1.2s linear infinite;
}
//-- 定义动画
@keyframes menu-animate {
    0% {
        opacity: 1;
    }
    50% {
        opacity: 0.8;
        box-shadow: 0 0 0 0.7vh var(--THEME-BACKGROUND), 0 0 0 1.1vh rgba(255, 55, 95, 1), 0 0 0 2.2vh var(--THEME-BACKGROUND), 0 0 0 2.6vh rgba(255, 55, 95, .7);
    }
    100% {
        opacity: 0.1;
        box-shadow: 0 0 0 1.7vh var(--THEME-BACKGROUND), 0 0 0 2.1vh rgba(255, 55, 95, 1), 0 0 0 3.2vh var(--THEME-BACKGROUND), 0 0 0 3.6vh rgba(255, 55, 95, .7);
    }
}

```
