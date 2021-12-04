# My-First-Repository
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<script>
function DisplayInput(){ 
    var nWNumber = document.getElementById("num1").value; 
    alert(nWNumber) 
} 

function ShowResult() {
    var nWNumber = document.getElementById("num1").value; 
    alert(nWNumber); 
    document.getElementById("result").innerHTML = String(nWNumber); 
}
function dectoBinary(number) { 
    var dcimal = document.getElementById("num1").value;
    var c = 2;
    var b = null;
    var arr = [ ];

    while( c != 0) {  
        b = dcimal % 2;
        c = parseInt( dcimal / 2);
        dcimal = c
        arr.push(b);  // arr是一個未被處理的陣列，也就是是反的，因為每次結果都被放到最後面導致 1011 變成 1101
    }
    return arr.reverse().join("").toString(); // return 這邊用reverve反轉陣列，並且利用join方法在每個陣列元素中插入 "" 字串 並且轉換回字串回傳
} 


function onBtnClkSubmit(){ 
    let input =  document.getElementById("num1").value; 
    document.getElementById("result").innerHTML = dectoBinary(input); 
}
</script>
<body>
<label>Please input a decimal whole number</label> 
<input type = "text" id="num1" name = "num1"><br><br>
<p id="result">Press the submit button display result here</p>  
<button id="button" type="button" onclick="onBtnClkSubmit()">Submit</button> 
</body>

</html>
