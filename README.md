# core-code-from-scratch-readme

///Thuesday challenge///

1) Interpreted And Compiled Programming Languages

-Compiled langauges are those that can be read more directly by a machine's logical processor there is a "build" formed to execute a set of instructions the environment/machine need to construct the "build" every time you request the program to run 

-Interpreted languages use a structure and resources in a way where the machine is able to read and perform instructions line by line without the need
to read the whole of a "build" and can adopt to changes on the run like in pythoh, javascript and others

2) Is Java an interpreted or compiled langauge?

Java uses a process where there is first a source code is compiled to bytecode by an environment compiler
then the bytecode is executed or interpreted on the Java virtual machine , in the present Java virtual machines can use a "Just in time" compiulation of instructions to execute instructions on the fly.
Therefore it can be said that Java is both interpreted and compiled 

3) pseudocode- currency converter:

START

PRINT "Enter an ammount of dollars"

AMMOUT <-- GET

BTCVAL <-- 0.000033

CONVERSION<-- AMMOUNT * BTCVAL

PRINT "ammount is equal to $" CONVERSION

END 


4) Translate Date of birth to binary , we divide each number by 2 and leave a remainder for each of the non divisible by 2 operations
such as:
for example, 1993/2 =  remainder 1
             996 /2 =            0
             498 /2 =            0 
             249 /2 =            1
             124 /2 =            0
             62  /2 =            0
             31  /2 =            1
             15  /2 =            1
             7   /2 =            1
             3   /2 =            1
             1   / 2=            1
taking the numbers from the lowest result leaves us wi the answer of : 11111001001

5) MIPS challenge, display my name and make a program that adds 2 numbers


#Display my name 
.data

 nome: .asciiz "\nMy name is Daniel!\n"

.text 

 main:
li $v0, 4  
la $a0, nome 
syscall 

li $v0, 10 # terminate program
syscall

 #Add two numbers 

    .data
    numo1: .asciiz "Write your first number: "
    numo2: .asciiz "Write your second number: "
    resultado: .asciiz "the result of the sum is: "

    .text
    #get first number
    la $a0, numo1
    li $v0, 4
    syscall
    li $v0, 5
    syscall
    move $t0, $v0

    #get second number
    la $a0, numo2
    li $v0, 4
    syscall
    li $v0, 5
    syscall
    move $t1, $v0

    #calculate and show a result
    la $a0, resultado
    li $v0, 4
    syscall
    add $t2, $t0, $t1
    move $a0, $t2
    li $v0, 1
    syscall

    #finalize program
    li $v0, 10
    syscall

/// print even numbers ////
 cont = 0

while ( cont <= 99 )  {
  cont++ 

if (cont % 2 == 0 ) {

  console.log(cont);
 }
}

//////////bad code 1 fixed with correct == operator/////////

var cond = false;

if ((cond == true)) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}

/////////////////////


///////Bad code 2 fixed using && operator 

var n = 200;

if (n == 100) {
  console.log('This is a special number!');
}
else 
if (n < 1000 && n % 10 == 0 ) {
  console.log('this number is almost special');
} else
  console.log('Just a regular number');
/////////////////////////




//////////////WEEK 2

////////Multiply 
function multiply(a, b){
  return a * b;
}


///////ASCII Total
function uniTotal (stre) {
  

  
let zum= 0;
  
  for ( let cont=0, charc= stre.length; cont < charc; cont++ ){ 

   zum+= stre[cont].charCodeAt();


}
  
return zum;
 }


///return ascii codefrom character 
function getChar(c){
  

let charz= String.fromCharCode(c) // 
  
  return charz
}



///////////student final grade
function finalGrade (exam, projects) {

  if (exam > 90 || projects>10 ) {FG=100;} else
   if (exam > 75 && projects >= 5)
      {FG=90;} else 
        if (exam > 50 && projects >= 2)
      {FG=75;} else 
      {FG=0;} 
return FG// final grade
}

/////////////////

///Holiday excercise 

function dutyFree(normPrice, discount, hol){
var descuento = normPrice * (discount / 100);
  var cantBot = hol / descuento;
  
  return Math.floor(cantBot);
}

/////twice as old

function twiceAsOld(dadYearsOld, sonYearsOld) {


 return Math.abs(dadYearsOld - 2 * sonYearsOld);
}

////valid spacing 
function validSpacing(string) {
 if(!string) {
    return true
  }
///check if position at the startincludes a space, initial position includes a spae or otherwise for consecutive spaces  
  if(string[0].includes(' ') || string[string.length -1].includes(' ') || string.includes('  ')) {
   return false
 } else {
   return true
 }}
 
 //Fake binary
//using .replace to 'replace' sets below and above 5 as needed
function fakeBin(numo){
  return numo.replace(/[1234]/g, '0').replace(/[56789]/g, '1')
}

///remove ! from end of string
function remove (string) {  
 let result = string;

  while (result[result.length - 1] === "!") {
    result = result.slice(0, -1);
  }

  
  return result;
}

////shortcut 


function shortcut (string) {
const str = string;
///use replace with needed set of vowels to remove and join result as cutWord

const cutWord = str.replace(/[aeiou]/gi, '');  

return cutWord;
}

/////rock, paper, scissors!

const rps = (p1, p2) => {
  
   if (p1 === p2) {
    return 'Draw!';
  }  if (p1 === 'rock' && p2 === 'scissors') {
   
 return 'Player 1 won!';
  } else if (p1 === 'paper' && p2 === 'rock') {

    return 'Player 1 won!';
  } else if (p1 === 'scissors' && p2 === 'paper') {

    return 'Player 1 won!';
  } else {

    return 'Player 2 won!';
  }
};
