<h1 align="center">Welcome to Quiz Project! 👋</h1>

# Quiz

In this project, we wrote a quiz program with html css and js

## Skills

Html , Css , Js

## Usage

We first wrote the questions and answer as an array in JavaScript
```JavaScript
var soal =['کدام زبان در پلتفرم وب اجرا میشود؟',
            'کدام زبان برنامه نویسی نیست؟',
            'با اچ تی ام ال کدام کار را نمیشود انجام داد؟',
            'جاوا اسکریپت چه زمانی به وجود آمد؟'];

var javab = [['جاوا','سی','پایتون','جاوا اسکریپت',3],
            ['HTML','JAVA','JS','GO',0],
            ['طراحی صفحات وب','برنامه نویسی ویندوز','اپلیکیشن PWA','برنامه تحت وب',1],
            ['1996','1995','1994','2000',1],
            ];
```

Next, we took the ID of each question section and displayed the question in that section

```JavaScript
var soal_html= document.getElementById("soal");
var javab1 = document.getElementById("jj1");
var javab2 = document.getElementById("jj2");
var javab3 = document.getElementById("jj3");
var javab4 = document.getElementById("jj4");

soal_html.innerText= soal[0];
javab1.innerText= javab[0][0];
javab2.innerText= javab[0][1];
javab3.innerText= javab[0][2];
javab4.innerText= javab[0][3];
console.log(javab);
```
Then we wrote a function that checks the correct answer and displays the results to the user

```JavaScript
var ic=0;
var dorost=0;

function ejra(){           
var j1= document.getElementById('j1').checked;
var j2= document.getElementById('j2').checked;
var j3= document.getElementById('j3').checked;
var j4= document.getElementById('j4').checked;

if (ic<4 && j1 == false && j2 == false && j3 == false && j4 == false){
    return;
}

if (ic==0 && j4==true) {dorost=dorost + 1;} 
if (ic==1 && j1==true) {dorost=dorost + 1;} 
if (ic==2 && j2==true) {dorost=dorost + 1;} 
if (ic==3 && j2==true) {dorost=dorost + 1;}  

ic= ic+1;
console.log(dorost , (ic))

if (ic>4){
    window.location.reload();
}

if (ic>3){
    soal_html.innerText ="جواب صحیح شما: " + dorost.toString() + ' از '+ ic.toString() + " سوال ";
                
    document.getElementById("javabha").style.display='none';
    document.getElementById("dokme").innerText='آزمون مجدد';
}else{
    soal_html.innerText= soal[ic];
    javab1.innerText= javab[ic][0];
    javab2.innerText= javab[ic][1];
    javab3.innerText= javab[ic][2];
    javab4.innerText= javab[ic][3];
}

document.getElementById('j1').checked=false;
document.getElementById('j2').checked=false;
document.getElementById('j3').checked=false;
document.getElementById('j4').checked=false;
}
```

## Result

This project was written by Majid Tajanjari and the Aiolearn team, and we need your support!❤️

# آزمون

در این پروژه یک برنامه مسابقه با html css و js نوشتیم

## مهارت ها

Html , Css , Js

## نحوه استفاده

ابتدا سوالات و پاسخ ها را به صورت آرایه ای در جاوا اسکریپت نوشتیم

```JavaScript
var soal =['کدام زبان در پلتفرم وب اجرا میشود؟',
            'کدام زبان برنامه نویسی نیست؟',
            'با اچ تی ام ال کدام کار را نمیشود انجام داد؟',
            'جاوا اسکریپت چه زمانی به وجود آمد؟'];

var javab = [['جاوا','سی','پایتون','جاوا اسکریپت',3],
            ['HTML','JAVA','JS','GO',0],
            ['طراحی صفحات وب','برنامه نویسی ویندوز','اپلیکیشن PWA','برنامه تحت وب',1],
            ['1996','1995','1994','2000',1],
            ];
```

بعد شناسه هر قسمت سوال را گرفتیم و سوال را در آن قسمت نمایش دادیم

```JavaScript
var soal_html= document.getElementById("soal");
var javab1 = document.getElementById("jj1");
var javab2 = document.getElementById("jj2");
var javab3 = document.getElementById("jj3");
var javab4 = document.getElementById("jj4");

soal_html.innerText= soal[0];
javab1.innerText= javab[0][0];
javab2.innerText= javab[0][1];
javab3.innerText= javab[0][2];
javab4.innerText= javab[0][3];
console.log(javab);
```
سپس تابعی نوشتیم که پاسخ صحیح را بررسی می کند و نتایج را به کاربر نمایش می دهد

```JavaScript
var ic=0;
var dorost=0;

function ejra(){           
var j1= document.getElementById('j1').checked;
var j2= document.getElementById('j2').checked;
var j3= document.getElementById('j3').checked;
var j4= document.getElementById('j4').checked;

if (ic<4 && j1 == false && j2 == false && j3 == false && j4 == false){
    return;
}

if (ic==0 && j4==true) {dorost=dorost + 1;} 
if (ic==1 && j1==true) {dorost=dorost + 1;} 
if (ic==2 && j2==true) {dorost=dorost + 1;} 
if (ic==3 && j2==true) {dorost=dorost + 1;}  

ic= ic+1;
console.log(dorost , (ic))

if (ic>4){
    window.location.reload();
}

if (ic>3){
    soal_html.innerText ="جواب صحیح شما: " + dorost.toString() + ' از '+ ic.toString() + " سوال ";
                
    document.getElementById("javabha").style.display='none';
    document.getElementById("dokme").innerText='آزمون مجدد';
}else{
    soal_html.innerText= soal[ic];
    javab1.innerText= javab[ic][0];
    javab2.innerText= javab[ic][1];
    javab3.innerText= javab[ic][2];
    javab4.innerText= javab[ic][3];
}

document.getElementById('j1').checked=false;
document.getElementById('j2').checked=false;
document.getElementById('j3').checked=false;
document.getElementById('j4').checked=false;
}
```

## نتیجه

این پروژه توسط مجید تجن جاری و تیم Aiolearn نوشته شده است و ما به حمایت شما نیازمندیم!❤️