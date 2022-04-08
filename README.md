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
