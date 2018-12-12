This folder includes the sample code to illustrate
the basic syntax of the language.

abstact types:

    object abstractTypes extends Application {
      abstract class Buffer {
        type T; val element: T
      }
      abstract class SeqBuffer {
        type T; val element: Seq[T]; def length = element.length
      }
      def newIntBuffer(el: Int) = new Buffer {
        type T = Int; val element = el
      }
      def newIntBuffer(el: Int*) = new SeqBuffer {
        type T = Int; val element = el
      }
      println(newIntBuffer(1).element)
      println(newIntBuffer(1, 2, 3).length)
    }
    Printer-friendly versionPrinter-friendly version

arrays:

    object ArrayDemo {
       def main(args: Array[String]) {
          var myList = Array(1.9, 2.9, 3.4, 3.5)

        // Print all the array elements
        for ( x <- myList ) {
           println( x )
        }

        // Summing all elements
        var total = 0.0;

        for ( i <- 0 to (myList.length - 1)) {
           total += myList(i);
        }
        println("Total is " + total);

        // Finding the largest element
        var max = myList(0);

        for ( i <- 1 to (myList.length - 1) ) {
           if (myList(i) > max) max = myList(i);
        }

        println("Max is " + max);
     }
  }
  
  variables:
  
                      object Demo {
                              def main(args: Array[String]) {
                                    var myVar :Int = 10;
                                    val myVal :String = "Hello Scala with datatype declaration.";
                                    var myVar1 = 20;
                                    val myVal1 = "Hello Scala new without datatype declaration.";

                                    println(myVar); println(myVal); println(myVar1); 
                                    println(myVal1);
                                 }
                              }
