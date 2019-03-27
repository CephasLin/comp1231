```javascript
function oppCase(string4,pos){
    let s = '';
    if(pos==="odd"){
        for(let i = 0; i<string4.length;i++){
            if(i%2==1){
                s+= string4[i];
            }
            if(i%2==0)
            {
                let n = string4.charCodeAt(i);
                if(n>=97 && n<=122){
                    s+= String.fromCharCode(n-32);
                }
                if(n>=65 && n<=90){
                    s+= String.fromCharCode(n+32);
                }
                else
                {
                    s+= String.fromCharCode(n);
                }
            }  
        }
    }
    if(pos==="even"){
        for(let i = 0; i<string4.length;i++){
            if(i%2==0){
                s+= string4[i];
            }
            if(i%2==1){
                let n = string4.charCodeAt(i);
                if(n>=97&&n<=122){
                    s+= String.fromCharCode(n-32);
                }
                if(n>=65 && n<=90){
                    s+= String.fromCharCode(n+32);
                }
                else{
                    s+= String.fromCharCode(n);
                }
            }  
        }
    }
    return s;
    
}
