# Dom-jQuery-
//DOM对象获取、事件绑定
var btnObj1 = document.getElementByID("btn");
btnObj1.onclick(匿名函数);

//jQuery对象获取、事件绑定
var btnObj2 = $("btn");
btnObj2.click(匿名函数);

//DOM对象与jQuery对象不同，二者的属性和方法不能交替使用；

//DOM对象转换为jQuery对象
$(btnObj1)

//jQuery对象转换为DOM对象
btnObj2[0]


//DOM事件加载，赋值的，后者会覆盖前者
window.onload = function () {
console.log("hellow,world");
};
window.onload = function () {
console.log("hellow again");
};
//jQuery事件加载，执行函数，二者都会执行
//方法1,页面全部加载完成后执行，速度最慢
$(window).load(function () {
console.log("hellow,world");
});
$(window).load(function () {
console.log("hellow again");
});

//方法2，页面中的基本元素加载完成后就执行，比方法1快
$(document).ready(function () {
console.log("hellow,world");
});
$(document).ready(function () {
console.log("hellow again");
});

//方法3，页面中的基本元素加载完成后就执行，同上
jQuery(function () {
console.log("hellow,world");
});
jQuery(function () {
console.log("hellow again");
});
