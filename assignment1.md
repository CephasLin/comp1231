```javascript
[Project link](https://codepen.io/frank_lin/pen/OqwWBy)

let task1 = document.getElementById("task_1");
function random(number){
    var s = '';
    var randomChar = function(){
        var n = Math.floor(Math.random()*62);
        if(n<10) return n;
        if(n<36) return String.fromCharCode(n+55);
        return String.fromCharCode(n+61);
    } 
    for(let i = 0; i< number; i++)
    {
        s += randomChar() ;  
    }
    return s;
}
task1.innerHTML+=random(5);

let task2 = document.getElementById("task_2");
function uppercase(string2){
    let s ='';
    for(let i = 0; i<string2.length;i++){
        n = string2.charCodeAt(i);
        s += String.fromCharCode(n-32);
    }
    return s;
}

task2.innerHTML +=uppercase('kitty');

let task3 = document.getElementById("task_3");
function addSpace(string3, num3){
    let s = '';
    for(let i = 0 ; i < num3; i++){
        s+= '&nbsp';
    }
    for(let j=0; j < string3.length;j++){
        s+=string3[j];
        
    }
    for(let i = 0 ; i < num3; i++){
        s+= '&nbsp';
    }
    return s;
}
task3.innerHTML += addSpace('Space',2);

let task4 = document.getElementById("task_4");
function oppCase(string4,pos){
    let s = '';
    if(pos=='odd'){
        for(let i = 0; i<string4.length;i++){  
            if(i%2==1){
                s+= string4[i];
            }else{
                let n = string4.charCodeAt(i);
                if(n>97){
                    s+= String.fromCharCode(n-32);
                }
                else{
                    s+= String.fromCharCode(n+32);
                }
            }  
        }
    }
    if(pos=='even'){
        for(let i = 0; i<string4.length;i++){
            if(i%2==0){
                s+= string4[i];
            }else{
                let n = string4.charCodeAt(i);
                if(n>97){
                    s+= String.fromCharCode(n-32);
                }
                else{
                    s+= String.fromCharCode(n+32);
                }
            }  
        }
    }
    return s;
    
}
task4.innerHTML += oppCase('AbcD','even');

let task5 = document.getElementById("task_5");
function reverse(string5){
    let s = '';
    for(let i =string5.length-1; i>=0;i--){
        s+= string5[i];
    }
    return s;
}
task5.innerHTML += reverse("abc");

/*let task6 = document.getElementById("task_6");
function conca(string6,string61){
    let s = '';
    
}*/
let task7=document.getElementById("task_7");
function removeFrontSpace(string7){
    let s = '';
    for(let i = 0; i < string7.length;i++){
        let n = string7.charCodeAt(i);
        if(n>=32){
            s+= string7[i];
        }
    }
    return s; 
}
task7.innerHTML +=removeFrontSpace("\nvalue \ta");

let task8 = document.getElementById("task_8");
function removeSpace(string8){
    let s = '';
    for(let i = 0; i < string8.length;i++){
        let n = string8.charCodeAt(i);
        if(n!=9 && n!=10 && n!=32){
            s+=string8[i];
        }
    }
    return s;
}
task8.innerHTML += removeSpace("\n value \t abc");

