______________________________
# ***CoreCode From Scratch Readme*** :computer:
#### **Developer:** *Ismael Cerrato* :boy:
______________________________
![](https://www.thepostcity.com/wp-content/uploads/2020/12/Become-a-Web-Developer.jpg)
______________________________

### **Tabla de Contenido**
______________________________
   1. [Week 1 - Introduction to programming & Javascript](#week1)
   2. [Week 2 - JavaScript](#week2)
   3. [Week 3 - JavaScript](#week3)
   4. [Week 4 - End Of Month & Pause Day](#week4)
   5. [Week 5 - TypeScript](#week5)
______________________________

![](https://www.trazos-web.com/wp-content/uploads/2020/03/los-40-mejores-blogs-sobre-diseno-y-desarrollo-web-en-espanol-1024x384.jpg)


______________________________
______________________________
______________________________

## :calendar: Week 1 - Introduction to programming & Javascript <a name="week1"></a>
### :triangular_flag_on_post: Tuesday Challenges :muscle:
:small_orange_diamond: **Answer to Question #1** 

*Compiled lenguages are those programming lenguages witch need a pre revision or translation fron a source to a program file (compile process) So, this type of lenguages need to be translating first and then can be reading by the computer. This lenguages needs a specific type of ending code to run in a specific platform
In the case of the interpreted lenguages, are translate step by step (line by line) and can be send the final code to any platform to execute.* 

:small_orange_diamond: **Answer to Question #2** 

*Java is both type, compiled and interpreted, because depends the platform or the necesity in the moment of execution, can be compile first and then be excecute, but, also can be interpreted because the java's compiler can create a bytecode file, which can be read by a intepreter after by the java virtual machine.*

:small_orange_diamond: **Excersice #3 - Pseudocode currency converter**

*You have been selected to develop the algorithm that will be used to convert dollars (USD) to bitcoin (BTC), for this the first thing you must do is deliver a pseudocode with the algorithm to be developed, in this way you can explain in a better way to the team what will be the required operation. The main idea is to have a website where the user will be asked to enter the amount to convert.*

* Pseudocode:
	* START
  	* GET dolaramount
   	* bit <-- 0.000022
  	* total <-- dolaramount / bit
  	* PRINT total
  	* END

### :triangular_flag_on_post: Wednesday Challenges :muscle:
:small_orange_diamond: **Exercise #1 - Your date of birth in the matrix?**
*Your team has just seen the movie "Matrix" and you have been asked, how the number of your year of birth would be written in binary. You must learn how to translate your date of birth into binary and show your team. (Do not use a webpage or a tool to convert your date of birth)*

  * START
  * GET year
  * temp <-- year
  * INIT bin 
  * START CICLE
  * temp <-- temp / 2
  	* START DESICION
  	* SI remain(temp/2) igual 0
  		* bin <-- concatenar(0, bin)
  	* SINO
  		* bin <-- concatenar(1, bin)
  	* END DESICION
  * END CICLE
  * PRINT BIN
  * END
 
:small_orange_diamond: **Exercise #2 - MIPS**
**Part 1** *Create a program that adds any two given numbers provided by the user*
```assembly
.data
	title: .asciiz "|---SUMA DE DOS NUMEROS---|\n"
	num1: .asciiz "\nIngrese el Primer Numero:"
	num2: .asciiz "\nIngrese el Segundo Numero:"
	result: .asciiz "\nEl resultado de la suma es:"
.text
	main:
	li $v0, 4
	la $a0, title
	syscall

	li $v0, 4
	la $a0, num1
	syscall

	li $v0, 5
	syscall
	
	move $t0, $v0

	li $v0, 4
	la $a0, num2
	syscall
	
	li $v0, 5
	syscall
	
	move $t1, $v0
	
	add $t2, $t0, $t1
	
	li $v0, 4
	la $a0, result
	syscall
	
	li $v0, 1
	move $a0, $t2
	syscall
```
**Part 2** *Create a program that displays your name*
``` assembly
.data
		name: .asciiz "Jos?? Ismael cerrato Ort??z\n"
	.text
		main:
		li $v0, 4
		la $a0, name
		syscall
```

## :triangular_flag_on_post: Thursday Challenges :muscle:
:small_orange_diamond: **Exercise #1 - Print special numbers** *In this exercise you must use an iterative flow control to be able to print all the even numbers in the range of numbers from 0 to 100. Remember that you should not print each number, you should use a flow control structure to perform the exercise*
```javascript
var num = 0;
while (num<100)
{
    num = num +2;
    console.log(num);
}
```

:small_orange_diamond: **Exercise #2 - Bad code** *The error in the code is the equal sign '='. when we use just one equals sign (=) is to asigment a value to a variable, when we want to compare two or more values, we use double equals sign (==)*
```javascript	
var cond = false;
if ((cond == true)) {
  console.log('The cond variable is true');
} 
else {
  console.log('The cond variable is false');
}
```

:small_orange_diamond: **Exercise #3 - Bad code 2** *You must create the code that follows the following logic, if the given number is 100, take this number as special and show the following message: "This is a special number!", but if the number is less than 1000, multiple of 10 and different from 100, you must show the following message: "This number is almost special". if none of the given conditions are met show the following message: "Just a regular number". Another developer was trying to program the logic, but apparently couldn't, you need to fix the code to work properly*
```javascript
var n = 0;
if (n == 100) {
    console.log('This is a special number!');
}
else{
    if ((n < 1000) && (n % 10 == 0)) {
        console.log('This number is almost special');
    } 
    else {
        console.log('Just a regular number');
    }
}
```
____________________________________________
____________________________________________
____________________________________________

## :calendar: Week 2 - Javascript <a name="week2"></a>
### :triangular_flag_on_post: Tuesday Challenges :muscle:
:small_orange_diamond: **Multiply exercise** 

*for solve this kata, only have to add the command RETURN in the second line*
```javascript
function multiply(a, b){
   return a * b;
}	

```
:small_orange_diamond: **ASCII Total**

*You'll be given a string, and have to return the sum of all characters as an int. The function should be able to handle all ASCII characters. For this Kata, i used FOR and the function charCodeAt()*
```javascript
function uniTotal (cadena) {
  let total = 0;
  for (let i = 0; i < cadena.length; i++)
  {
    total = total + Number(cadena.charCodeAt(i));
  }
  return total;
}
```
:small_orange_diamond: **Char From ASCII Value**

*Write a function get_char() / getChar() which takes a number and returns the corresponding ASCII char for that value. In this case i have used the method String.fromCharCode()*
```javascript
function getChar(c){
    let text = String.fromCharCode(c);
    return text;
}
```
:small_orange_diamond: **Binary Addition**

*Implement a function that adds two numbers together and returns their sum in binary. The conversion can be done before, or after the addition. The binary number returned should be a string.*
```javascript
function addBinary(a,b) {
    var suma = a + b;
    var binario = '';
    var numTemp = suma;
    while (suma != 0){
        numTemp = Math.trunc(suma / 2);
        if ((suma % 2) == 0){
           binario = '0'+ binario;
        }
	else{
            binario = '1'+ binario;
        }
        suma = numTemp;
    }
    return binario;
}
```
:small_orange_diamond: **Student's Final Grade**

*Create a function finalGrade, which calculates the final grade of a student depending on two parameters: a grade for the exam and a number of completed projects.
* This function should take two arguments: exam - grade for exam (from 0 to 100); projects - number of completed projects (from 0 and above);
* This function should return a number (final grade). There are four types of final grades:
	* 100, if a grade for the exam is more than 90 or if a number of completed projects more than 10.
	* 90, if a grade for the exam is more than 75 and if a number of completed projects is minimum 5.
	* 75, if a grade for the exam is more than 50 and if a number of completed projects is minimum 2.
	* 0, in other cases
```javascript
function finalGrade (exam, projects) {
  if (exam>90 || projects>10)
    {
      return 100;
    }else if (exam>75 && projects>=5){
      return 90;
    }else if (exam>50 && projects>=2){
      return 75;
    }else{
      return 0;
    }
}
```
### :triangular_flag_on_post: Wednesday Challenges :muscle:
:small_orange_diamond: **Holiday VIII - Duty Free**

*The purpose of this kata is to work out just how many bottles of duty free whiskey you would have to buy such that the saving over the normal high street price would effectively cover the cost of your holiday.You will be given the high street price (normPrice), the duty free discount (discount) and the cost of the holiday.For example, if a bottle cost ??10 normally and the discount in duty free was 10%, you would save ??1 per bottle. If your holiday cost ??500, the answer you should return would be 500.All inputs will be integers. Please return an integer. Round down.*
```javascript
function dutyFree(normPrice, discount, hol){
  let cant1 = (normPrice*discount)/100;
  let cant2 = hol/cant1;
  let cant3 = Math.floor(cant2);
  return cant3;
}
```
:small_orange_diamond: **Twice as old**

*Your function takes two arguments:*
  * current father's age (years)
  * current age of his son (years)
*??alculate how many years ago the father was twice as old as his son (or in how many years he will be twice as old).*
```javascript
function twiceAsOld(dadYearsOld, sonYearsOld) {
  let edad = sonYearsOld * 2;
  let diferencia = 0;
  if (edad < dadYearsOld){
    diferencia = dadYearsOld - edad;
  } else {
    diferencia = edad - dadYearsOld;
  }
  return diferencia
}
```
:small_orange_diamond: **Valid Spacing**

*Our task is to write a function called valid_spacing() or validSpacing() which checks if a string has valid spacing. The function should return either true or false (or the corresponding value in each language).For this kata, the definition of valid spacing is one space between words, and no leading or trailing spaces. Words can be any consecutive sequence of non space characters.*
```javascript
function validSpacing(s) {
    for(let i=0;i<=s.length;i++){
        if (s[0]==' ' || s[s.length-1]==' '){
            var validation = false;
	} else if (s[i]==' ' && s[ i + 1 ]==' ' && i >= 0 && i<s.length - 1 || s[i] == ' ' && s[ i - 1 ] == ' ' && i > 0 && i <= s.length - 1){ 
	var validation = false;
	}
    }
    if (typeof(validation) == "undefined"){
        return true;
    } else {return false};
}
``` 
:small_orange_diamond: **Fake Binary**

*Given a string of digits, you should replace any digit below 5 with '0' and any digit 5 and above with '1'. Return the resulting string. Note: input will never be an empty string*
```javascript
function fakeBin(x){
  let digito = '';
  let binario = '';
  for (let i = 0; i < x.length; i++){
    digito = x.substr(i,1);
    if (digito < 5){
      binario = binario + '0';
    } else {
      binario = binario + '1';
    }
  }
  return binario;
}
```
### :triangular_flag_on_post: Thursday Challenges :muscle:
:small_orange_diamond: **Exclamation marks series #2: Remove all exclamation marks from the end of sentence**
*Remove all exclamation marks from the end of sentence*
```javascript
function remove (string) {  
  let contador = string.length;
  let letra = '';
  let text = string;
  while (contador > 0){
    letra = string.substr(contador-1,1);
    if (letra === '!'){
      text = string.substr(0,contador);
    } else{
      text = string.substr(0,contador);
      break;
    }
    contador = contador -1;
  }
  return text;
}
```
:small_orange_diamond: **Vowel Remove**

*Create a function called shortcut to remove the lowercase vowels (a, e, i, o, u ) in a given string.*
```javascript
function shortcut(string) {  
  let vocales = ['a','e','i','o','u'];
  let letra = '';
  let texto = '';
  let centil = false;
  for (let i = 0; i < string.length; i++){
    letra = string.charAt(i);
    centil = vocales.includes(letra,0);
    if (centil === false){
      texto = texto + letra;
    }
  }
  return texto;
}
```
:small_orange_diamond: **Rock Paper Scissors**

*Let's play! You have to return which player won! In case of a draw return Draw!.*
```javascript
const rps = (p1, p2) => {
  let result = '';
  if (p1 === p2){
    result = 'Draw!';
  }else if (p1 === 'scissors'){
    if (p2 === 'paper'){
      result = 'Player 1 won!';
    } else {
      result = 'Player 2 won!';
    }
  }else if (p1 === 'paper'){
    if (p2 === 'rock'){
      result = 'Player 1 won!';
    } else {
      result = 'Player 2 won!';
    } 
  } else if (p1 === 'rock'){
    if (p2 === 'scissors'){
      result = 'Player 1 won!';
    } else {
      result = 'Player 2 won!';
    } 
  }
  return result;
};
```
:small_orange_diamond: **Persistent Bugger.**

*Write a function, persistence, that takes in a positive parameter num and returns its multiplicative persistence, which is the number of times you must multiply the digits in num until you reach a single digit.*
```javascript
function persistence(num) {
  let digito = num.toString().split('');
  let contador = 0;
  while (digito.length > 1){
    let multi = 1;
    for (let i = 0; i < digito.length; i++ ){
      multi = multi * digito[i];
    }
    contador = contador + 1;
    digito = multi.toString().split('');
  }
  return contador;
}
```
____________________________________________
____________________________________________
____________________________________________

## :calendar: Week 3 - Javascript <a name="week3"></a>
### :triangular_flag_on_post: Monday Challenges :muscle:
:small_orange_diamond: **Who Likes this?** 

*You probably know the "like" system from Facebook and other pages. People can "like" blog posts, pictures or other items. We want to create the text that should be displayed next to such an item.Implement the function which takes an array containing the names of people that like an item.*
```javascript
function likes(names) {
  let tamano = names.length;
  if (tamano === 0){return 'no one likes this';}
  else if (tamano === 1){return `${names[0]}${' likes this'}`;} 
  else if (tamano === 2){return `${names[0]}${' and '}${names[1]}${' like this'}`;}
  else if (tamano === 3){return `${names[0]}${', '}${names[1]}${' and '}${names[2]}${' like this'}`;}
  else{ 
    tamano = tamano - 2;
    return `${names[0]}${', '}${names[1]}${' and '}${tamano}${' others like this'}`;
  } 
}
```
:small_orange_diamond: **BitCounting**

*Write a function that takes an integer as input, and returns the number of bits that are equal to one in the binary representation of that number. You can guarantee that input is non-negative. Example: The binary representation of 1234 is 10011010010, so the function should return 5 in this case*
```javascript
var countBits = function(n) {
  let bin = 0;
  let bina = '';
  let rem, i = 1, step = 1;
  while (n != 0) {
     rem = n % 2;
     n = parseInt(n / 2);
     bin = bin + rem * i;
     bina = bina + rem.toString();
     i = i * 10;
  }
  let contador = 0;
  for (let j = 0; j < bina.length; j++){
    if (bina.charAt(j) === '1'){
      contador = contador + 1;
    }
  }
  return contador;
};
```
:small_orange_diamond: **Your order, please**

*Your task is to sort a given string. Each word in the string will contain a single number. This number is the position the word should have in the result.Note: Numbers can be from 1 to 9. So 1 will be the first word (not 0).If the input string is empty, return an empty string. The words in the input String will only contain valid consecutive numbers.*
```javascript
function order (words){
  let palabras = words.split(' '); 
  let orden = [];
  let num = 0;
  let regex = /(\d+)/g;
  let resultado = '';
  for (let i = 0; i < palabras.length-1; i++){
    orden.push('');
  }
  for (let j = 0; j < palabras.length; j++){
    num = parseInt(palabras[j].match(regex));
    orden[num-1] = (palabras[j]);
    resultado = orden.join(' ');
    }
  return resultado;
}
```

### :triangular_flag_on_post: Tuesday Challenges :muscle:
:small_orange_diamond: **Simple Pig Latin** 

*Move the first letter of each word to the end of it, then add "ay" to the end of the word. Leave punctuation marks untouched.*

```javascript
function pigIt(str){
  let signos = ['!', '??', '?', '??', '.', ',', ':', ';'];
  let palabras = str.split(' ');
  let palabra = '';
  let resultado = [];
  
  for (let j = 0; j < palabras.length; j++){
    palabra = palabras[j];
    if (signos.indexOf(palabra) >= 0){
        resultado.push(`${palabra.substring(1, (palabra.length))}${palabra.substring(0,1)}`); 
    }else{
      resultado.push(`${palabra.substring(1, (palabra.length))}${palabra.substring(0,1)}${'ay'}`);
    }
  }
 return resultado.join(' ');  
}
```
:small_orange_diamond: **Count the number of Duplicates** 

*Write a function that will return the count of distinct case-insensitive alphabetic characters and numeric digits that occur more than once in the input string. The input string can be assumed to contain only alphabets (both uppercase and lowercase) and numeric digits.*

```javascript
function duplicateCount(text) {
  let lettlers = text.toLowerCase().split('').sort();
  let i = 0,
    amount = 0,
    lastIndexOfChar = 0;
  while (lettlers.length) {
    lastIndexOfChar = lettlers.lastIndexOf(lettlers[i]);
    if (lastIndexOfChar !== i) {
      i = lastIndexOfChar;
      amount++;
    }
    lettlers = lettlers.slice(++i);
    i = 0;
  }
  return amount;
}
```
:small_orange_diamond: **Decode the Morse code** 

*In this kata you have to write a simple Morse code decoder. While the Morse code is now mostly superseded by voice and digital data communication channels, it still has its use in some applications around the world. The Morse code encodes every character as a sequence of "dots" and "dashes". For example, the letter A is coded as ?????, letter Q is coded as ???????????, and digit 1 is coded as ??????????????. The Morse code is case-insensitive, traditionally capital letters are used. When the message is written in Morse code, a single space is used to separate the character codes and 3 spaces are used to separate words. For example, the message HEY JUDE in Morse code is ???????? ?? ???????????   ??????????? ??????? ??????? ??.
NOTE: Extra spaces before or after the code have no meaning and should be ignored.
In addition to letters, digits and some punctuation, there are some special service codes, the most notorious of those is the international distress signal SOS (that was first issued by Titanic), that is coded as ?????????????????????. These special codes are treated as single special characters, and usually are transmitted as separate words.
Your task is to implement a function that would take the morse code as input and return a decoded human-readable string.*

```javascript
decodeMorse = function (morseCode) {
  morseCode = morseCode.replace(/   /g, ' # ');
  let c_Morse = morseCode.split(' ');
  let texto = ''
  for (let i = 0; i < c_Morse.length; i++){
    if (c_Morse[i] === '#'){
      texto = texto + ' ';
    } else if(MORSE_CODE[c_Morse[i]] !== undefined){
      texto = texto + MORSE_CODE[c_Morse[i]];
    }
  }
  return texto.trim(); 
};
```

### :triangular_flag_on_post: Wednesday Challenges :muscle:
:small_orange_diamond: **Valid Parentheses** 

*Write a function that takes a string of parentheses, and determines if the order of the parentheses is valid. The function should return true if the string is valid, and false if it's invalid.*

```javascript
function validParentheses(parens){
  var n = 0;
  for (var i = 0; i < parens.length; i++) {
    if (parens[i] == '(') n++;
    if (parens[i] == ')') n--;
    if (n < 0) return false;
  }
  
  return n == 0;
}
```

:small_orange_diamond: **Convert string to camel case** 
*Complete the method/function so that it converts dash/underscore delimited words into camel casing. The first word within the output should be capitalized only if the original word was capitalized (known as Upper Camel Case, also often referred to as Pascal case).*

```javascript
function toCamelCase(str){
  if (str.length === 0){return '';}
  
  str = str.replace(/-/g,' ');
  str = str.replace(/_/g,' ');
  let strArray = str.split(' ');
  let textoFinal = strArray[0];
  
  for (let i = 1; i < strArray.length; i++){
    let palabra = strArray[i];
    textoFinal = textoFinal + palabra.charAt(0).toUpperCase() + palabra.slice(1);
  }
  return textoFinal;
}
```

:small_orange_diamond: **Unique In Order** 
*Implement the function unique_in_order which takes as argument a sequence and returns a list of items without any elements with the same value next to each other and preserving the original order of elements.*

```javascript
var uniqueInOrder=function(iterable){
  let resultado = [];
  let ultimoDato = '';
  
  for (let i = 0; i < iterable.length; i++){
    if (iterable[i] === ultimoDato){
      continue;
    }  
      else{
        ultimoDato = iterable[i];
        resultado.push(iterable[i]);
    }
  }
  return resultado;
}
```

### :triangular_flag_on_post: Thursday Challenges :muscle:
:small_orange_diamond: **Fold an array**

*In this kata you have to write a method that folds a given array of integers by the middle x-times.An example says more than thousand words:*
```
Fold 1-times:
[1,2,3,4,5] -> [6,6,3]

A little visualization (NOT for the algorithm but for the idea of folding):

 Step 1         Step 2        Step 3       Step 4       Step5
                     5/           5|         5\          
                    4/            4|          4\      
1 2 3 4 5      1 2 3/         1 2 3|       1 2 3\       6 6 3
----*----      ----*          ----*        ----*        ----*

Fold 2-times:
[1,2,3,4,5] -> [9,6]
```
*As you see, if the count of numbers is odd, the middle number will stay. Otherwise the fold-point is between the middle-numbers, so all numbers would be added in a way.
The array will always contain numbers and will never be null. The parameter runs will always be a positive integer greater than 0 and says how many runs of folding your method has to do.
If an array with one element is folded, it stays as the same array.
The input array should not be modified!*

```javascript
function foldArray(array, runs) {
  if (array.length === 1) return array;
  let output = [...array];
  let aheadPosition = 0;
  while (runs) {
    if (output.length === 1) return output;
    output = Array.from(
      { length: Math.round(output.length / 2) },
      (v) => 0
    ).map((v, i) => {
      aheadPosition = output.length - (i + 1);
      if (aheadPosition === i) return output[i];
      return output[i] + output[aheadPosition];
    });
    runs--;
  }
  return output;
}
```

:small_orange_diamond: **Encrypt this!**

*You want to create secret messages which can be deciphered by the Decipher this! kata. Here are the conditions:
Your message is a string containing space separated words.
You need to encrypt each word in the message using the following rules:
The first letter must be converted to its ASCII code.
The second letter must be switched with the last letter
Keepin' it simple: There are no special characters in the input.*

```javascript
var encryptThis = function(text) {
  const encriptar = text.split(' ');
  
  let encriptado = [];
  
  for (let i = 0; i < encriptar.length; i++){
    let palabra = encriptar[i];
    if (palabra.length === 1){ 
      encriptado.push(palabra.charCodeAt());
      continue;
    }
    else if (palabra.length === 2){ 
      encriptado.push(`${palabra.charCodeAt(0)}${palabra[1]}`)
      continue
    }
    else {
    encriptado.push(`${palabra.charCodeAt(0)}${palabra[palabra.length - 1]}${palabra.slice(2, palabra.length - 1)}${palabra[1]}`);
    }
  }
  return encriptado.join(' ');
}
```
____________________________________________
____________________________________________
____________________________________________

## :calendar: Week 4 - End Of Month & Pause Day <a name="week4"></a>
### :triangular_flag_on_post: Wednesday Challenges :muscle:
:small_orange_diamond: **Simple validation of a username with regex** 

*Write a simple regex to validate a username. Allowed characters are:
-lowercase letters,
-numbers,
-underscore
Length should be between 4 and 16 characters (both included).*

```javascript
function validateUsr(username) {
  res =  /^([a-z]+|\d+|_){4,16}$/.test(username) 
  return res
}

```

:small_orange_diamond: **Get number from string**

*Write a function which removes from string all non-digit characters and parse the remaining to number. E.g: "hell5o wor6ld" -> 56*

```javascript
function getNumberFromString(s) {
  return Number(s.replace(/\D/g,''));
}
```

### :triangular_flag_on_post: Thusday Challenges :muscle:
:small_orange_diamond: **String cleaning**

*Your harried co-workers are looking to you for a solution to take this garbled text and remove all of the numbers. Your program will take in a string and clean out all numeric characters, and return a string with spacing and special characters ~#$%^&!@*():;"'.,? all intact.*

```javascript
function stringClean(s) {
  return s.replace(/[0-9]/g, '');
}
```

:small_orange_diamond: **String cleaning**

*You need to write regex that will validate a password to make sure it meets the following criteria:
At least six characters long
contains a lowercase letter
contains an uppercase letter
contains a number
Valid passwords will only be alphanumeric characters.*

```javascript
function validate(password) {
  return (
    /^[A-Za-z0-9]{6,}$/.test(password) &&
    /[A-Z]+/.test(password) &&
    /[a-z]+/.test(password) &&
    /[0-9]+/.test(password)
  );
}
```

## :calendar: Week 5 - TypeScript <a name="week5"></a>
### :triangular_flag_on_post: Monday Challenges :muscle:
:small_orange_diamond: **Find the missing letter**

*Write a method that takes an array of consecutive (increasing) letters as input and that returns the missing letter in the array. You will always get an valid array. And it will be always exactly one letter be missing. The length of the array will always be at least 2.
The array will always contain letters in only one case.*

```javascript
function findMissingLetter(array) {
  for (let i = 0; i < array.length; i++) {
    if (array[i].charCodeAt() + 1 !== array[i + 1].charCodeAt()) {
       return String.fromCharCode(array[i].charCodeAt() + 1);
    }
  }
}
```
:small_orange_diamond: **Reverse or rotate?**

*The input is a string str of digits. Cut the string into chunks (a chunk here is a substring of the initial string) of size sz (ignore the last chunk if its size is less than sz).
If a chunk represents an integer such as the sum of the cubes of its digits is divisible by 2, reverse that chunk; otherwise rotate it to the left by one position. Put together these modified chunks and return the result as a string.
If
	sz is <= 0 or if str is empty return ""
	sz is greater (>) than the length of str it is impossible to take a chunk of size sz 		hence return "".*

```javascript

```
