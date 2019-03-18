```javascript
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



