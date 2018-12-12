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


 >> - ### Interactive mode ### - Here the user codes and runs directly in the command prompt
 >>> To open scala in the command prompt use the following  command.
 >>>  ```
 >>>  \>scala
 
 >>> The following should be displayed
 >>>  ```
 >>>  Welcome to Scala version 2.9.0.1
 >>>  Type in expressions to have them evaluated.
 >>>  Type :help for more information.
 
 >>>  Type the following text to the right of the Scala prompt and press the Enter key −
 >>>  ```
 >>>  scala> println("Hello, Scala!");
 
 >>>  The following will be outputed
 >>>  ```
 >>>  Hello, Scala!
 
 >> - ### Script mode ### -Here the user codes in a file then compiles and executes the file from the command prompt
 >>> **HiWorld**
 >>> ```scala
 >>>  object HiWorld {
 >>>  /* This is my first java program.  
 >>>  * This will print 'Hi World' as the output
 >>>  */
 >>>  def main(args: Array[String]) {
 >>>      println("Hi, world!") // prints Hi World
 >>>  }
 >>> }
 
 >>>  The file is saved as **Hiworld.scala**
 
 >>>  Then open commmand promtpt and go to the directory where you saved the program
 Then '**scalac**' command is typed in fromt of the file **Hi.scala** in commmand prompt to compile the file.
 Since this is only bytecode whic will run in Java Virtual Machine (JVM) using '**scala**' command.
 >>>   ```
 >>>   \> scalac HiWorld.scala
 >>>   \> scala HiWorld
 
 >>>   The above command is used to compile and execute the Scala program. And output 
 >>>   ```
 >>>   Hi, World!
 
 >>> **Syntax and conding conventions**
  >>>> - **Method Names** − All method names must begin with a Lower Case letter. If multiple words are used to form the name of the method, then each inner word's first letter should be in Upper Case. For example ' def myMethodName() '
  >>>> - **Identifiers** - In Scala names are required for all components, and the names used for objects, methods, classes and  variables are called identifiers. Since Scala is case sensitive keywoords cannot be used and an identifier.
 >>>> - **Class Names** − For all class names, the first letter should be in Upper Case. If several words are used to form a name of the class, each inner word's first letter should be in Upper Case.
 >>>> - **Program File Name** − Name of the program file should exactly match the object name. When saving the file you should save it using the object name (Remember Scala is case-sensitive) and append ‘.scala’ to the end of the name. (If the file name and the object name do not match your program will never compile). In essence if the object name is 'HelloWord' the file must be saved as 'HelloWorld.scala'
 >>>> - **def main(args: Array[String])** − Scala program processing starts from the main() method which is a mandatory part of every Scala Program.
 >>>>- **Case Sensitivity** − Scala is case-sensitive, which means identifier hello and Hello have completely different meanings in Scala
 >>>>> - **Operator Identifiers** - These kind of Identifiers consists of the printable ASCII characters such as +,-,?,: or #.And they could consist of one or more operator characters.
 >>>>>   ```
 >>>>>   + ++ ::: <?> :>
 >>>>> - **Alphanumeric Identifiers** - These kind of Identifiers could either start with a letter or and underscore, which other letters or underscore and digits could follow up. The the symbol '$" is restricted and should not be used in Scala as it is a reserved keyword.
 >>>>>   ```scala
 >>>>>   age, _value, salary, _1_value.
 >>>>> - **Literal Identifiers** - These are basically arbitrary string enclosed in back ticks (`...`)
 >>>>>   ```
 >>>>>   `x `<clinit>` `yield`
 >>>>> - **Mixed Identifiers** - A mixed identifier consists of an alphanumeric identifier, then an underscore and a operator identifier
 >>>>>   ```scala
 >>>>>   unary_+,  myvar_=
 
 >>> **Comments, Newline Characters, Blank Lines and Whitespace in Scala**
 >>>> - Comments - In Scala single-line and multiple-line comments are supported in a very similar way to Java. All characters available inside any comment are ignored by Scala compiler. So it is important that multi-line comments be nested, and are required to be nested properly.
 >>>> **HelloWorld**
 >>>> ```scala
 >>>>  object HelloWorld {
 >>>>  /* This is my first java program.  
 >>>>  * This will print 'Hello World' as the output
 >>>>  */
 >>>>  def main(args: Array[String]) {
 >>>>      println("Hello, world!") 
 >>>>  }
 >>>> }
 >>>> // Output - Hello, world
 
 >>>> - Newline Characters - Since Scala is line-oriented language where statements may be terminated by semicolons (;) or newlines. It has a very similar approach to this like as that of Java
 >>>>   ```
 >>>>   val g = "hello"; println(g)
 >>>> - Blank Lines and Whitespace - In Scala lines containing only whitespace, could possibly be with a comment, is known as a blank line, and Scala totally ignores it while running the program. Tokens may be separated by whitespace characters and/or comments.

>>> **Variables**- In Scala variables can have three different scopes depending on the place where they are being used. The could exist as fields, as methods parameters and as local variables. Scalar has different synatax for variable declaration. It goes from **nutable variables** with the keyword being **var**;
>>>>  ```
>>>>  var myVar : String = "Foo"
>>>>  var dVar : String - "Fee"
>>> to **immutable variables** with the keyword being **val**;
>>>> ````
>>>>  val myVal : String = "Foo"
>>>>  val dVal : String - "Fee"
>>> Scala also supports variable type inference and Multiple assignments such as tuples

>>> **Conditions and Boolen expression**- Like in Java, Scala similarly has the same concepts of conditions;
>>>> - **If Statement** - if the Boolean expression evaluates to true then the block of code inside the ‘if’ expression will be executed. If not, the first set of code after the end of the ‘if’ expression (after the closing curly brace) will be executed.
>>>>  ```scala
>>>>  object Demo {
>>>>     def main(args: Array[String]) {
>>>>        var x = 10;
>>>>        if( x < 20 ){ //if (boolean_expression)
>>>>           println("This is if statement"); //Statements will execute if the Boolean expression is true
>>>>        }
>>>>     }
>>>>  }
>>>>  // Output - This is if statement

>>>> - **If-else Statement** - if An ‘if’ statement can be followed by an optional else statement, which executes when the Boolean expression is false.
>>>>  ```scala
>>>>  object Demo {
>>>>     def main(args: Array[String]) {
>>>>        var x = 10;
>>>>        if( x < 20 ){ //if (boolean_expression)
>>>>           println("This is if statement"); //Statements will execute if the Boolean expression is true
>>>>        }else {
>>>>           println("This is else statement"); //Statements will execute if the Boolean expression is false
>>>>        }
>>>>     }
>>>>  }
>>>>  // Output - This is else statement      

>>>> **if-else-if-else Statement** -
>>>>  ```scala
>>>>  object Demo {
>>>>     def main(args: Array[String]) {
>>>>        var x = 10;
>>>>        if( x == 20 ){ //if (boolean_expression)
>>>>           println("This is if statement"); //Statements will execute if the Boolean expression is true
>>>>        }else  if(x == 10){
>>>>           println("This is else-if statement"); //Statements will execute if the Boolean expression is true
>>>>        }else{
>>>>           println("This is else statement"); // Statement will execute if the Boolean expression is false
>>>>        }
>>>>     }
>>>>  }
>>>> // Output - This is else-if statement
>>> Scala also hosts nested conditions like 'if' and 'else' statement within themselves

>>> **Loop** - In every language various controls structures exists to execute blocks of code several number of times that is why loop statements exists in Scala.
>>>> **For Loop** - Executes a sequence of statements multiple times and abbreviates the code that manages the loop variable.
>>>>   ``` 
>>>>   for( var x <- Range ){
>>>>      statement(s); }
>>>>   for(var x <- List ){
>>>>      statement(s); }

>>>>   ```scala
>>>>   object Demo {
>>>>      def main(args: Array[String]) {
>>>>         var a = 0;
>>>>         var b = 0; val numList = List(4,5,6);
>>>>      // for loop execution with a range and List
>>>>         for( a <- 1 to 3){ println( "Value of a: " + a ); }
>>>>         for( a <- numList){println( "Value of b: " + b ); }
>>>>      }
>>>>   }
>>>>  //Output
>>>>  value of a: 1
>>>>  value of a: 2
>>>>  value of a: 3
>>>>  value of b: 4
>>>>  value of b: 5
>>>>  value of b: 6
>>> Scala also hosts nested for loop and loops with conditions similiar to what is seen in Java
>>>> **while Loop** - It tests the condition before executing the loop body and repeats the statement or group of statements while a given condition is true.
>>>>   ```
>>>>   while(condition){
>>>>     statement(s);}

>>>>   ```scala
>>>>   object Demo {
>>>>      def main(args: Array[String]) {
>>>>     // Local variable declaration:
>>>>        var a = 11;
>>>>         // while loop execution
>>>>        while( a < 16 ){
>>>>           println( "Value of a: " + a );
>>>>           a = a + 1;
>>>>        }
>>>>      }
>>>>    }
>>>>  //Output
>>>>  value of a: 11
>>>>  value of a: 12
>>>>  value of a: 13
>>>>  value of a: 14
>>>>  value of a: 15
>>>
>>>> **do-while** -  It tests for the condition at the bottom oof the loop, unlike the while loop that checks for the condition at the top of the loop.
>>>>   ```
>>>>   do{
>>>>     statement(s);
>>>>   }
>>>>   while(condition);

>>>>   ```scala
>>>>   object Demo {
>>>>      def main(args: Array[String]) {
>>>>      // Local variable declaration:
>>>>         var a = 11;
>>>>     // do loop execution
>>>>         do {
>>>>            println( "Value of a: " + a );
>>>>            a = a + 1;
>>>>        }
>>>>        while( a < 15 )
>>>>     }
>>>>   }
>>>>  //Output
>>>>  value of a: 11
>>>>  value of a: 12
>>>>  value of a: 13
>>>>  value of a: 14
>>>>  value of a: 15


>>> **Functions**
>>>> Declaration
>>>> ```scala
>>>>    def functionName ([list of parameters]) : [return type]

>>>> Definition
>>>> ```
>>>>    def functionName ([list of parameters]) : [return type] = {
>>>>      function body
>>>>      return [expr]
>>>>    }

>>>> Implementation
>>>> ```scala
>>>>    object add {
>>>>       def addInt( a:Int, b:Int ) : Int = {
>>>>          var sum:Int = 0
>>>>          sum = a + b
>>>>          return sum
>>>>       }
>>>>    }

>>>> Calling functions
>>>> ```scala
>>>>    object Demo {
>>>>       def main(args: Array[String]) {
>>>>          println( "Returned Value : " + addInt(5,7) );
>>>>       }   
>>>>       def addInt( a:Int, b:Int ) : Int = {
>>>>          var sum:Int = 0
>>>>          sum = a + b
>>>>         return sum
>>>>       }
>>>>    }
>>>>    Output - Return Value : 12

>>> **Files I/O**
>>>> Writing from a scala file called Demo.scala to a text file called Demo.txt
>>>> ```scala
>>>>    import java.io._
>>>>     object Demo {
>>>>        def main(args: Array[String]) {
>>>>           val writer = new PrintWriter(new File("test.txt" ))
>>>>           writer.write("Hello Scala")
>>>>           writer.close()
>>>>       }
>>>>     }
>>>>    // Output - Hello Scala
>>>> Reading from the Demo.txt  file through the Demo.scala file to the command prompt
>>>> ```scala
>>>>    import scala.io.Source
>>>>    object Demo {
>>>>       def main(args: Array[String]) {
>>>>          println("Following is the content read:" )
>>>>          Source.fromFile("Demo.txt" ).foreach { 
>>>>             print 
>>>>          }
>>>>       }
>>>>     }
>>>>    // Output-
>>>>    Following is the content read:
>>>>    Hello Scala


## About the tools

> _Describe the compiler or interpreter needed_.
>> - In the IDE Eclipse there is an extension for Scala. This Scala IDE for Eclipse provides dedicated support for developing pure Scala and mixed applications. Scala IDE 3.0 offers a whole host of tools and features to make life easier for developers, this consists of the advanced editing tools including code completion, implicit and semantic highlighting to all new indent guide. To top it off there is even a shiny Scala debugger along with a few notable bug fixes, with a reliable Junit test finder and an asynchronous debugger. Furthermore JDK and its standard library is required to run Scala programs compiled by Eclipse.
>> - IntelliJ IDEA is technically an IDE for Java, though the IDE provides support for lots of other languages like Scala, Groovy, Kotlin, JavaScript, TypeScript and SQL. In addition to the host of features, IntelliJ IDEA offers Scala-specific support in testing with ScalaTest. This makes it easier for developers to perform unit testing with ease. Other interesting features include smart completion, language injection, an editor-centric environment, and lots of useful build tools. Lastly it uses Java's Development kit and standard library in the compilation and execution.


## About the standard library
### Functions
>>  The standard library inclcudes various packages that useful for multiple function use cases. One of such packages is the math package. It includes functions such as log, exp, sin, etc from **scala.math**
>>> **Exponential and Logarithmic** - uses number data type to perform math arithmetics of exponential or Logarithmic respectively
>>> ```scala
>>> def log(x: Double): Double
>>> def exp(x: Double): Double

>>> **Rounding** - rounds number data types in function respective directions
>>> ```scala
>>> def floor(x: Double): Double
>>> def ceil(x: Double): Double

>>> **Minimum and Maximum** - finds the min or max of two numbers depending on the funciton call
>>> ```scala
>>> def min(x: Double, y: Double): Double
>>> def max(x: Double, y: Double): Double

### Data Structures
>>  The standard library inclcudes various packages that useful for multiple data structure use cases. One of such packages is the math package. It includes data structures such as list, maps, sets, vectors, etc from **scala.collection.immutable**

## About open source library
>> - briefly about the scala community - The Scala open source community is a very diverse community, where people from all over the world contribute their work to benefit the community as a whole
>> - Play framework as a contribution by the community - One of such contributions by the community is the Play web framework. Play is a high-productivity Java and Scala web application framework that integrates the components and APIs you need for modern web application development
>> - Features of play framework
>>   * It is developer friendly as it supports type safety, built in testing tools and IDEs such as Eclipse and Intellij IDEA
>>   * It uses a fully asynchronous model built on top of Akka
>>   * It is stateless and scales simply and predictably
>>   * It was built primarly for needs of mobile apps & modern web
>> - Who uses Play framework
>>   - EA 
>>   - verizon 
>>   - Walmart
>>   - Linkedin 
>>   - Samsung

# Analysis of the language
>> **The style of programming supported by the language: functional vs procedural programming**
>>> _One of Scala’s perks is that its functional programming functionality with an OOP style._


>> **The ability to perform meta-programming such as macros**
>>> _Pattern matching in Scala is no joke. Scala uses the match statement for this purpose, which is a powerful version of Java's switch statement. It allows you to match on any type of data, lists, and even your own types. If you haven't already tried it, I suggest you play around with it a little._

>> **Symbol resolution and its support for closure**
>>> _Simple symbol resolutions are by far the most common. In this case, two symbols with similar characteristics are detected, with one symbol taking precedence over the other. This symbol resolution is carried out silently by the link-editor. For example, with symbols of the same binding, a symbol reference from one file is bound to a defined, or tentative symbol definition, from another file. Or, a tentative symbol definition from one file is bound to a defined symbol definition from another file. This resolution can occur between two relocatable objects, or between a relocatable object and the first definition found in a shared object dependency._

>>> _Symbols that undergo resolution can have either a global or weak binding. Within relocatable objects, weak bindings have lower precedence than global binding. Relocatable object symbols with different bindings are resolved according to a slight alteration of the basic rules. Weak symbols can usually be defined through the compiler, either individually or as aliases to global symbols._


>>> _Complex symbol resolutions occur when two symbols of the same name are found with differing attributes. In these cases, the link-editor generates a warning message, while selecting the most appropriate symbol. This message indicates the symbol, the attributes that conflict, and the identity of the file from which the symbol definition is taken. In the following example, two files with a definition of the data item array have different size requirements._

>> **Scoping rules supported by the language: lexical vs dynamic scoping**
>>> _The scoping rules supported by the language is lexical._

>> **Functional programming constructs either as part of the language or supported by the standard library of the runtime**

>>> _It allows you to interact seamlessly with standard Java libraries while developing from a functional perspective._


>> **Its type system: static vs dynamic types**
>>> _Scala is statically typed and compiles down to the same fast bytecode as Java so its usually about as fast as Java (sometimes a little faster sometimes a little slower). e.g. compare how well Scala does in some benchmarks with groovy or jruby. Or this. Note speed isn't everything - there are times when you might want to trade code thats 10x slower for more productivity and conciseness; but for a long term replacement for javac speed is important.
Yet Scala has type inference - so its typically as concise as Ruby/Groovy but that everything has static types. This is a good thing; it makes code comprehension, navigation & documentation much simpler. Any token/method/symbol you can click on to navigate to the actual implementation code & documentation. No wacky monkey patching involved, or doubting of who added a method, when and how - which is great for large projects with lots of folks working on the same code over long periods of time. Scala seems to hit the perfect sweet spot between the consise feel of a dynamic language, while actually being completely statically typed. So I never have to remember the magic methods that are available - or run a script in a shell then inspect the object to see what it really looks like - the IDE/compiler just knows while you edit._


>> **Strengths and weaknesses of the language**
>>> _Weakness_
>>>> - Slow Compilation- In the world of coding speed in very important and Scala is slow in comparison to Java and Kotlin, which runs in second where as it runs in seconds.
>>>> - Binary Compilation in Challenging- for a few versions. Let us say you compiled with Scala 2.11 the same would not compile with 2.1.
>>>> - Less Efficient in the Management of Null Safety._

>>> _Strength_
>>>> - Simple and straightforward syntax- Scala typically requires two-thirds less code than Java. The syntax is also more flexible. For example, you can leave out periods between method calls so the code is more human-readable and easier to understand.
>>>> - Inherently immutable objects- Scala’s programming language reduces many thread-safety concerns that spring up in traditional Java applications.
>>>> - Highly functional- Scala treats functions as first-class citizens.
>>>> - Fast implementation speed- It allows for quicker implementation and enhanced performance.
>>>> - It is fun- Scala challenges strong engineers in a meaningful and entertaining manner, making development more fun.
>>>> - Easy to solve concurrency issues. It has an Actor library to solve concurrency problems more rapidly.
>>>> - XML support. Scala supports XML, which is beneficial if you have a need to encode documents in your products._
