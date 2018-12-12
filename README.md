Scala
- shane rego
- shane.rego@uoit.net

## About the language

> _Describe the language_
>
> - History

            - Scala was created by Martin Odersky.It was initially designed at the École Polytechnique Fédérale de Lausanne in the year 2001 and initially released in the year 2003, and it only surfaced to the public in the year 2004. Scala was originally released on the Java platform as a general-purpose programming language.
            The name Scala is an abbreviation of "scalable" , it represents a language that is scalable according to the needs of its users.
> - Some interesting features

            -Scala was designed to address critisims of Java,everything is made to look like an object.
            Import statements can be anywhere and streams process big data (or infinite data) efficiently


## About the syntax

> _give some code snippet of the language_
-Scala has two modes an interactive and a script mode
Interactive mode ### - Here the user codes and runs directly in the command prompt
To open scala in the command prompt use the following command.

\>scala
The following should be displayed if Scala is installed in your system.

Welcome to Scala version 2.9.0.1
Type in expressions to have them evaluated.
Type :help for more information.
Type the following text to the right of the Scala prompt and press the Enter key −

scala> println("Hello, Scala!");
The following result will be produced

Hello, Scala!
Script mode ### -Here the user codes in a file then compiles and executes the file from the command prompt
HelloWorld

 object HelloWorld {
 /* This is my first java program.  
 * This will print 'Hello World' as the output
 */
 def main(args: Array[String]) {
     println("Hello, world!") // prints Hello World
 }
}
The file is saved as Helloworld.scala Then open commmand promtpt and go to the directory where you saved the program Then 'scalac' command is typed in fromt of the file Helloworld.scala in commmand prompt to compile the file. Since this is only bytecode whic will run in Java Virtual Machine (JVM) using 'scala' command.

\> scalac HelloWorld.scala
\> scala HelloWorld
The above command is used to compile and execute the Scala program. And output

Hello, World!
Syntax and conding conventions

Case Sensitivity − Scala is case-sensitive, which means identifier hello and Hello have completely different meanings in Scala.
Class Names − For all class names, the first letter should be in Upper Case. If several words are used to form a name of the class, each inner word's first letter should be in Upper Case.
Program File Name − Name of the program file should exactly match the object name. When saving the file you should save it using the object name (Remember Scala is case-sensitive) and append ‘.scala’ to the end of the name. (If the file name and the object name do not match your program will never compile). In essence if the object name is 'HelloWord' the file must be saved as 'HelloWorld.scala'
def main(args: Array[String]) − Scala program processing starts from the main() method which is a mandatory part of every Scala Program.
Method Names − All method names must begin with a Lower Case letter. If multiple words are used to form the name of the method, then each inner word's first letter should be in Upper Case. For example ' def myMethodName() '
Identifiers - In Scala names are required for all components, and the names used for objects, methods, classes and variables are called identifiers. Since Scala is case sensitive keywoords cannot be used and an identifier.
Operator Identifiers - These kind of Identifiers consists of the printable ASCII characters such as +,-,?,: or #.And they could consist of one or more operator characters.
+ ++ ::: <?> :>
Alphanumeric Identifiers - These kind of Identifiers could either start with a letter or and underscore, which other letters or underscore and digits could follow up. The the symbol '$" is restricted and should not be used in Scala as it is a reserved keyword.
age, _value, salary, _1_value.
Literal Identifiers - These are basically arbitrary string enclosed in back ticks (...)
`x `<clinit>` `yield`
Mixed Identifiers - A mixed identifier consists of an alphanumeric identifier, then an underscore and a operator identifier
unary_+,  myvar_=
Comments, Newline Characters, Blank Lines and Whitespace in Scala

Comments - In Scala single-line and multiple-line comments are supported in a very similar way to Java. All characters available inside any comment are ignored by Scala compiler. So it is important that multi-line comments be nested, and are required to be nested properly. HelloWorld
 object HelloWorld {
 /* This is my first java program.  
 * This will print 'Hello World' as the output
 */
 def main(args: Array[String]) {
     println("Hello, world!") 
 }
}
// Output - Hello, world
Newline Characters - Since Scala is line-oriented language where statements may be terminated by semicolons (;) or newlines. It has a very similar approach to this like as that of Java
val g = "hello"; println(g)
Blank Lines and Whitespace - In Scala lines containing only whitespace, could possibly be with a comment, is known as a blank line, and Scala totally ignores it while running the program. Tokens may be separated by whitespace characters and/or comments.
Variables- In Scala variables can have three different scopes depending on the place where they are being used. The could exist as fields, as methods parameters and as local variables. Scalar has different synatax for variable declaration. It goes from nutable variables with the keyword being var;

var myVar : String = "Foo"
var dVar : String - "Fee"
to immutable variables with the keyword being val;

 val myVal : String = "Foo"
 val dVal : String - "Fee"
Scala also supports variable type inference and Multiple assignments such as tuples

Conditions and Boolen expression- Like in Java, Scala similarly has the same concepts of conditions;

If Statement - if the Boolean expression evaluates to true then the block of code inside the ‘if’ expression will be executed. If not, the first set of code after the end of the ‘if’ expression (after the closing curly brace) will be executed.
object Demo {
   def main(args: Array[String]) {
      var x = 10;
      if( x < 20 ){ //if (boolean_expression)
         println("This is if statement"); //Statements will execute if the Boolean expression is true
      }
   }
}
// Output - This is if statement
If-else Statement - if An ‘if’ statement can be followed by an optional else statement, which executes when the Boolean expression is false.
object Demo {
   def main(args: Array[String]) {
      var x = 10;
      if( x < 20 ){ //if (boolean_expression)
         println("This is if statement"); //Statements will execute if the Boolean expression is true
      }else {
         println("This is else statement"); //Statements will execute if the Boolean expression is false
      }
   }
}
// Output - This is else statement      
if-else-if-else Statement -

object Demo {
   def main(args: Array[String]) {
      var x = 10;
      if( x == 20 ){ //if (boolean_expression)
         println("This is if statement"); //Statements will execute if the Boolean expression is true
      }else  if(x == 10){
         println("This is else-if statement"); //Statements will execute if the Boolean expression is true
      }else{
         println("This is else statement"); // Statement will execute if the Boolean expression is false
      }
   }
}
// Output - This is else-if statement
Scala also hosts nested conditions like 'if' and 'else' statement within themselves

Loop - In every language various controls structures exists to execute blocks of code several number of times that is why loop statements exists in Scala.

For Loop - Executes a sequence of statements multiple times and abbreviates the code that manages the loop variable.

for( var x <- Range ){
   statement(s); }
for(var x <- List ){
   statement(s); }
object Demo {
   def main(args: Array[String]) {
      var a = 0;
      var b = 0; val numList = List(4,5,6);
   // for loop execution with a range and List
      for( a <- 1 to 3){ println( "Value of a: " + a ); }
      for( a <- numList){println( "Value of b: " + b ); }
   }
}
//Output
value of a: 1
value of a: 2
value of a: 3
value of b: 4
value of b: 5
value of b: 6
Scala also hosts nested for loop and loops with conditions similiar to what is seen in Java

while Loop - It tests the condition before executing the loop body and repeats the statement or group of statements while a given condition is true.

while(condition){
  statement(s);}
object Demo {
   def main(args: Array[String]) {
  // Local variable declaration:
     var a = 11;
      // while loop execution
     while( a < 16 ){
        println( "Value of a: " + a );
        a = a + 1;
     }
   }
 }
//Output
value of a: 11
value of a: 12
value of a: 13
value of a: 14
value of a: 15
do-while - It tests for the condition at the bottom oof the loop, unlike the while loop that checks for the condition at the top of the loop.

do{
  statement(s);
}
while(condition);
object Demo {
   def main(args: Array[String]) {
   // Local variable declaration:
      var a = 11;
  // do loop execution
      do {
         println( "Value of a: " + a );
         a = a + 1;
     }
     while( a < 15 )
  }
}
//Output
value of a: 11
value of a: 12
value of a: 13
value of a: 14
value of a: 15
Functions

Declaration

   def functionName ([list of parameters]) : [return type]
Definition

   def functionName ([list of parameters]) : [return type] = {
     function body
     return [expr]
   }
Implementation

   object add {
      def addInt( a:Int, b:Int ) : Int = {
         var sum:Int = 0
         sum = a + b
         return sum
      }
   }
Calling functions

   object Demo {
      def main(args: Array[String]) {
         println( "Returned Value : " + addInt(5,7) );
      }   
      def addInt( a:Int, b:Int ) : Int = {
         var sum:Int = 0
         sum = a + b
        return sum
      }
   }
   Output - Return Value : 12
Files I/O

Writing from a scala file called Demo.scala to a text file called Demo.txt

   import java.io._
    object Demo {
       def main(args: Array[String]) {
          val writer = new PrintWriter(new File("test.txt" ))
          writer.write("Hello Scala")
          writer.close()
      }
    }
   // Output - Hello Scala
Reading from the Demo.txt  file through the Demo.scala file to the command prompt
```scala
   import scala.io.Source
   object Demo {
      def main(args: Array[String]) {
         println("Following is the content read:" )
         Source.fromFile("Demo.txt" ).foreach { 
            print 
         }
      }
    }
   // Output-
   Following is the content read:
   Hello Scala


## About the tools

> _Describe the compiler or interpreter needed_.

## About the standard library

> _Give some examples of the functions and data structures
> offered by the standard library_.

## About open source library

> _Describe at least one contribution by the open source
community written in the language._

# Analysis of the language

> _Organize your report according to the project description
document_.


