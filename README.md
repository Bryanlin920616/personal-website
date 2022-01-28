# personal-website

<!-- css
    text-align: center ;對齊  左右置中
    text-indent 縮格
    text-transform: 切換大小寫
    text-decoration: 裝飾

    font-family:字體
    font-style:
    font-weight:粗度

    line-height:間距
    letter-spacing:
    word-spacing:
-->
<!-- box model 內往外 context->padding->border->margin
    xxx-top:
    xxx-right:
    xxx-bottum:
    xxx-left:
    padding: 上下 左右;
    padding: 上 右 下 左;
    border: width style color;
    border-radius: 圓角
    it would be okay to have a negative border
 -->


 <!-- Default display property 
Block: Always start a new line and takes full width (div h1 p )
Inline: Does not start a new one and only take up as much as content space
->display: inline(block); to change the status of inline or block  

->inline-block (像block一樣可以調整 padding margin 但仍保留inine的特性)


Horizontal centering
->margin: 0 auto;

ul li a {
    list style type: property
}

box-sizing: border-box; (fix the height & weight) to keep up your whole layout

universal selector *{}

display: none;
opacity:0; (0~1)不透明度
visibility: hidden;

background:url("image.png"); //default
background-repeat: xxx; //controll whether repeat or not
background-size: cover; big pic ->small pic(布滿整個畫面)
background-position: center(or more); 左上角(0,0) 右正下正
background-attachment: fixed; 保持背景不動
background: linear-gradient(red,green); 坡度default:由上到下 第一項加to top left(右下至左上) tool:CSS color gradient generator

add the hole text to the center
{
    display: flex;
    align-items: center;
    justify-content: center;
    text-align center;
}
---------------------------------------
{
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    background-attachment: fixed;
}={
    background: url("xxx") center/cover fixed no-repeat
}

float(類似word的靠圖片旁的效果) clear (回到原始的樣子 圖字分離)
overflow: hidden; 喀掉多餘的圖

-----不太懂
position: static;
position: relative;
position: absolute;
position: fixed; 給定位置 如:top:0 right:0


mid-width: (starting from)
max-width: (up to)->should be care about rewriting 

@media screen and (min-width: 675px){
    .one{
        //是螢幕大小改變畫面;
    }
}

z-index: 0;(處理重疊的順序) 
work if the image's position is absolute or relative
won't work if position is static

last rule order 採用最後一個指定的property

pseudo elements ::before ::after CONTENT not element 
content:'' ---- required 
img ---- does not work (img is a kind of content)

descendant and child combinators
.header h1 
div h1 
div > h1 

::first-line ::first-letter
:link :visited :hover :active

:root 1rem = 16px(default) depend on the root

transform:translate(X,Y)-移位,scale(X,Y)-縮放倍率,rotate(30deg)旋轉,skew(30deg,30deg)偏斜

transition:change over time
transition-property: 針對哪個屬性 A,B,C
transition-duration: 隔多久才要做改變 A,B,C
==transition: property duration delay
EX: 
.three{
    background: blue;
    transition: background 3s 2s,border-radius 3s 2s;
}
.three{
    border
}

how the transition take place 
transition-timing-function:
trasition:all 3s here 2s;
ease = default
ease = slow start, fast, slow end
linear = same speed start to end 
ease-in = slow start
ease-out = slow end 
ease-in-out = slow start, fast, slow end


transition 0 -> 100%
ANIMATION 0 1% 2% 3% ... 100%

EX:
.one{
    background: blue;
    animation-name: move;
    animation-duration: 5s;
    animation-iteration-count: 2;
    /* animation: move 5s infinite */
}

@keyframes move {
    0% {
        transform:translateX(20px) ;
    }
    50%{
        transform:translateX(50px);
        background: red;
    }
    100%{
        transform:translateX(-10px);
    }
}
animition-fill-mode: ...; 決定動畫結束後要停留在100%的畫面 還是初始畫面


:root { //global
    --varName1: xxx;
    --varName2: all 0.4s linear;
    --mainTransition: all 0.4 linear;  
}
.heading{
    color: var(--varName1);
    transition: var(--mainTransition);
}
.heading:hover{
    color: var(--varName2);
}

ICONS

text-shadow: 1px(x-axis) 1px(y-axis) 3px(blur) red(shadowColor)
box-shadow:
tools-> generator

HTML semantic 

emmet 
h1.one#one = <h1 class="one" id="one"></h1>
div>ul>li*2 =
    <div>
        <ul>
            <li></li>
            <li></li>
        </ul>
    </div> 

ul>li*5{$} = 
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
        <li>4</li>
        <li>5</li>
    </ul>
-->
