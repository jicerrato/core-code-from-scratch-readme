# core-code-from-scratch-readme
## Week 1 - Thursday
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

## Week 1 - Tuesday
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
	
## Week 2 - Thursday
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
