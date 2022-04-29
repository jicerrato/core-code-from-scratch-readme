# core-code-from-scratch-readme
## Week 1 - Tuesday
### Question #1
1.- Compiled lenguages are those programming lenguages witch need a pre revision or translation fron a source to a program file (compile process) So, this type of lenguages need to be translating first and then can be reading by the computer. This lenguages needs a specific type of ending code to run in a specific platform
In the case of the interpreted lenguages, are translate step by step (line by line) and can be send the final code to any platform to execute. 

### Question #2
2.- Java is both type, compiled and interpreted, because depends the platform or the necesity in the moment of execution, can be compile first and then be excecute, but, also can be interpreted because the java's compiler can create a bytecode file, which can be read by a intepreter after by the java virtual machine. 
### Excersice #3
3.- Pse
  1. START
  2. GET dolaramount
  3. bit <-- 0.000022
  4. total <-- dolaramount / bit
  5. PRINT total
  6. END

## Week 1 - Wednesday
### Exercise #1
  1. START
  2. GET year
  3. temp <-- year
  4. INIT bin 
  4. START CICLE
  5. --temp <-- temp / 2
  6. --START DESICION
  7. ----SI remain(temp/2) igual 0
  8. ------bin <-- concatenar(0, bin)
  9. ----SINO
  10. -----bin <-- concatenar(1, bin)
  11. --END DESICION
  12. END CICLE
  13. PRINT BIN
  14. END
### Exercise #2
#### Part 1
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
	
#### Part 2
	.data
		name: .asciiz "José Ismael cerrato Ortíz\n"
	.text
		main:
		li $v0, 4
		la $a0, name
		syscall

## Week 1 - Thursday
### Exercise #1
	var num = 0;

	while (num<100)
	{
	    num = num +2;
	    console.log(num);
	}
	
### Exercise #2
The error in the code is the equal sign '='. when we use just one equals sign (=) is to asigment a value to a variable, when we want to compare two or more values, we use double equals sign (==)
	var cond = false;

	if ((cond == true)) 
	{
	  console.log('The cond variable is true');
	} 
	else 
	{
	  console.log('The cond variable is false');
	}

### Exercise #3

	var n = 0;

	if (n == 100) 
	{
	    console.log('This is a special number!');
	}
	else
	{
	    if ((n < 1000) && (n % 10 == 0)) 
	    {
	        console.log('This number is almost special');
	    } 
	    else 
	    {
	        console.log('Just a regular number');
	    }
	}
	
## Week 2 - Tuesday
### Multiply exercise
for solve this kata, only have to add the command RETURN in the second line

	function multiply(a, b){
	  return a * b;
	}
	
### ASCII Total
You'll be given a string, and have to return the sum of all characters as an int. The function should be able to handle all ASCII characters. For this Kata, i used FOR and the function charCodeAt()

	function uniTotal (cadena) {
	  let total = 0;
	  for (let i = 0; i < cadena.length; i++)
	  {
	    total = total + Number(cadena.charCodeAt(i));
	  }
	  return total;
	}

### Char From ASCII Value
Write a function get_char() / getChar() which takes a number and returns the corresponding ASCII char for that value. In this case i have used the method String.fromCharCode()

	function getChar(c)
	{
	    let text = String.fromCharCode(c);
	    return text;
	}

### Binary Addition
Implement a function that adds two numbers together and returns their sum in binary. The conversion can be done before, or after the addition. The binary number returned should be a string.

	function addBinary(a,b) 
	{
	    var suma = a + b;
	    var binario = '';
	    var numTemp = suma;
	    while (suma != 0)
	    {
	        numTemp = Math.trunc(suma / 2);
	        if ((suma % 2) == 0)
	        {
	            binario = '0'+ binario;
	        }
	        else
	        {
	            binario = '1'+ binario;
	        }
	        suma = numTemp;
	    }
	    return binario;
	}

### Student's Final Grade
Create a function finalGrade, which calculates the final grade of a student depending on two parameters: a grade for the exam and a number of completed projects.

This function should take two arguments: exam - grade for exam (from 0 to 100); projects - number of completed projects (from 0 and above);

This function should return a number (final grade). There are four types of final grades:

100, if a grade for the exam is more than 90 or if a number of completed projects more than 10.
90, if a grade for the exam is more than 75 and if a number of completed projects is minimum 5.
75, if a grade for the exam is more than 50 and if a number of completed projects is minimum 2.
0, in other cases

	function finalGrade (exam, projects) {
	  if (exam>90 || projects>10)
	    {
	      return 100;
	    }
	  else if (exam>75 && projects>=5)
	    {
	      return 90;
	    }
	  else if (exam>50 && projects>=2)
	    {
	      return 75;
	    }
	  else
	    {
	      return 0;
	    }
	}

## Week 2 - Wednesday
### Holiday VIII - Duty Free
The purpose of this kata is to work out just how many bottles of duty free whiskey you would have to buy such that the saving over the normal high street price would effectively cover the cost of your holiday.
You will be given the high street price (normPrice), the duty free discount (discount) and the cost of the holiday.
For example, if a bottle cost £10 normally and the discount in duty free was 10%, you would save £1 per bottle. If your holiday cost £500, the answer you should return would be 500.
All inputs will be integers. Please return an integer. Round down.

	function dutyFree(normPrice, discount, hol)
	{
	  let cant1 = (normPrice*discount)/100;
	  let cant2 = hol/cant1;
	  let cant3 = Math.floor(cant2);
	  return cant3;
	}


### Twice as old
Your function takes two arguments:
 - current father's age (years)
 - current age of his son (years)
Сalculate how many years ago the father was twice as old as his son (or in how many years he will be twice as old).

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
	
### Valid Spacing
our task is to write a function called valid_spacing() or validSpacing() which checks if a string has valid spacing. The function should return either true or false (or the corresponding value in each language).
For this kata, the definition of valid spacing is one space between words, and no leading or trailing spaces. Words can be any consecutive sequence of non space characters. 

	function validSpacing(s) {
	    for(let i=0;i<=s.length;i++){
	        if (s[0]==' ' || s[s.length-1]==' '){
	            var validation = false;}
	        else if (s[i]==' ' && s[i+1]==' ' && i>=0 && i<s.length-1 || s[i]==' ' && s[i-			1]==' ' && i>0 && i<=s.length-1){
	            var validation = false;}
	    }
	    if (typeof(validation) == "undefined"){
	        return true;}
	    else {return false};
	}

### Fake Binary
Given a string of digits, you should replace any digit below 5 with '0' and any digit 5 and above with '1'. Return the resulting string. Note: input will never be an empty string

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

## Week 2 - Thursday
### Remove all exclamation marks from the end of sentence

	function remove (string) {  
	  let contador = string.length;
	  let letra = '';
	  let text = string;
	  while (contador > 0){
	    letra = string.substr(contador-1,1);
	    //console.log(letra);
	    if (letra === '!'){
	      text = string.substr(0,contador);
	    }else{
	      text = string.substr(0,contador);
	      break;
	    }
	    contador = contador -1;
	  }
	  return text;
	}
	
### Vowel Remove
Create a function called shortcut to remove the lowercase vowels (a, e, i, o, u ) in a given string.

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

### Rock Paper Scissors
Let's play! You have to return which player won! In case of a draw return Draw!.

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

### Persistent Bugger.
Write a function, persistence, that takes in a positive parameter num and returns its multiplicative persistence, which is the number of times you must multiply the digits in num until you reach a single digit.

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

##Week 3 - Monday
### Who Likes this?
You probably know the "like" system from Facebook and other pages. People can "like" blog posts, pictures or other items. We want to create the text that should be displayed next to such an item.Implement the function which takes an array containing the names of people that like an item. 

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


