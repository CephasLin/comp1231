```javascript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
    <h1>Array And Loops</h1>
    <div id="example_1"></div>
    <div id="example_2"></div>
    <div id="example_3"></div>
    <div id="example_4"><pre>
        Task 1
        Ask the user for the size of an array
        Create an empty array of the size specified above
        Fill the array with any default value for all indices</pre>
    </div>
    <div id="example_5">
        <pre>
        Task2
        Create an array that stores your 3 fav colors 
        Create another array that stores your 3 fav numbers
        Create a third array that merges the first two arrays
</pre>
    </div>
    <div id="example_6">
        <pre>
        Task3
        -Create a string with your student ID
        -Using a string method, Turn your student ID into an array with nine indices, 
        representing every digit of your student numbers. 
        Store this array to a new variable
        -Ouput the index position of the last occurance of a "1"
        -input any letter between the 3rd and 4th index of the array
        -remove the last element of the array
        </pre>
    </div>
    <div id="example_7"><pre>
        -Create a string with your student ID
        -Using a string method, split your student ID by the number '0'. 
         Store the array to a new variable.
        -remove the second and third elements on the array
        -remove the first element of the array
        -replace the last two elements with any other two values</pre></div>

    <div id="example_8">
    </div>

    <div id="example_9"></div>
    
    <script>
        let example_1 = document.getElementById("example_1");
        //create three value, each value is a unique data type
        let array_1  = ["hello", true, 1];
        
        example_1.innerHTML += array_1[0]+ "<br/>";
        example_1.innerHTML +="<hr>";

        for(let i = 0; i<array_1.length; i++){
            example_1.innerHTML += array_1[i] + "<br/>";
        }
        
        example_1.innerHTML +="<hr>";

        for(let i=array_1.length-1; i>=0; i--){
            example_1.innerHTML += array_1[i] + "<br/>";
        }

        let example_2 = document.getElementById("example_2");
        let array_2 = [];
        array_2['name'] = "comp1231";
        array_2['time'] = "10am";
        array_2['day_of_week'] = 5;
        array_2['love_JS'] = true;

        let array_3 = [];
        array_3[0] = "comp1231";
        array_3[1] = "10am";
        array_3[2] = 5;
        array_3[3] = true;

        example_2.innerHTML +="<hr>";
        //for(placeholder_value_representing_property_name IN collection)
        for(let prop in array_3){
            example_2.innerHTML += prop + ",";
           
            example_2.innerHTML += array_3[prop];
            example_2.innerHTML +="<br/>";
        }
        /*
        example_3.innerHTML += "<hr>";
        array_3.push = "Hello";
        example_3.innerHTML += array_3 + '<br/>';
        */
        example_3.innerHTML +="<hr>";
        let example_4 = document.getElementById('example_4');
        let n= parseInt(prompt("Enter an integer from 1-3"));
        let array_4 = [];
        for(i=0;i<n;i++){
            array_4[i]="hello ";
            example_4.innerHTML += array_4[i];
        }
        example_4.innerHTML +="<hr>";
        let example_5 = document.getElementById('example_5');
        let array_5=[];
        let array_5_2 = [];
        array_5[0] = "red";
        array_5[1] = "green";
        array_5[2] = "blue";
        array_5_2[0] = 1;
        array_5_2[1] = 2;
        array_5_2[2] = 3;
        let fav = array_5.concat(array_5_2);
        example_5.innerHTML += fav;
        example_5.innerHTML +="<hr>";
        
        
        let example_6 = document.getElementById('example_6');
        let str = '101198598'; //creating array using string
        let array_6 =[];//turn string into array
        for(let i=0; i<str.length;i++){
            array_6.push(str.charAt(i));
        }
        example_6.innerHTML += array_6 + '<br/>';
        
        //find the last "1"
        for(let i = array_6.length-1; i>=0; i--){
            if(array_6[i]==1){
                example_6.innerHTML += 'It\'s indice is:' +i +'<br/>'; 
                break;
            }
        }
        //insert an element to array
        example_6.innerHTML += "Original Array:" + array_6 + '<br/>';
        array_6.splice(3,0,"a");
        example_6.innerHTML += "Add a letter:" + array_6+ '<br/>';
        //delete the last element
        array_6.pop();
        example_6.innerHTML += "Original Array:" + array_6 + '<br/>';
        example_6.innerHTML += "<hr>";

        let example_7 = document.getElementById("example_7");
        let str2 = '10109090408';
        let array_7 = [];
        //split by the number 0;
            array_7 = str2.split("0");
        example_7.innerHTML += array_7 + '<br/>';

        //remove the second and third element
        //delete array_7[1]; delete only update the value to 0, doesn't change length
        array_7.splice(1,2);
        example_7.innerHTML += "Remove 2th, 3th:" + array_7 + '<br/>';
        //remove the first
        array_7.shift();
        example_7.innerHTML += "Remove 1st:" + array_7+ '<br/>';
        //replace the last two elements with any other two values.
        array_7[1]=2;
        array_7[2]=3;
        //array_7.copyWithin(1,0);
        example_7.innerHTML += "Replace:" + array_7 + '<br/>';
        example_7.innerHTML +="<hr>";
        
    </script>
</body>

</html>
