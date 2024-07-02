1>Bubble Sort Algorithm

def bubbleSort(arr: Array[Int]): Array[Int] = {
  for (i <- 0 until arr.length - 1) {
    for (j <- 0 until arr.length - i - 1) {
      if (arr(j) > arr(j + 1)) {
        val temp = arr(j)
        arr(j) = arr(j + 1)
        arr(j + 1) = temp
      }
    }
  }
  arr
}

// Example usage:
val arr = Array(64, 34, 25, 12, 22, 11, 90)
println(bubbleSort(arr).mkString(", "))

2>Write scala code to find the length of each word from the array.

val words = Array("apple", "banana", "cherry")
for(i <- 0 until words.length){
  println(words(i).length)
}

3> Write scala code to find the number of books published by each author, 
referring to the collection given below, with (authorName, BookName)
val books = List(
  ("Dr. Seuss", "How the Grinch Stole Christmas!"),
  ("Jon Stone", "Monsters at the End of This Book"),
  ("Dr. Seuss", "The Lorax"),
  ("Jon Stone", "Big Bird in China"),
  ("Dr. Seuss", "One Fish, Two Fish, Red Fish, Blue Fish")
)

val booksByAuthor = books.groupBy(_._1).map { case (author, books) => (author, books.size) }
println(booksByAuthor)

4>Pattern Matching with Case Classes
abstract class Notification
case class Email(sender: String, title: String, body: String) extends Notification
case class SMS(caller: String, message: String) extends Notification

def showNotification(notification: Notification): String = {
  notification match {
    case Email(sender, title, _) => s"You got an email from $sender with title: $title"
    case SMS(caller, message) => s"You got an SMS from $caller! Message: $message"
  }
}

// Example usage:
val someEmail = Email("john.doe@example.com", "Meeting Reminder", "Don't forget our meeting at 10 AM.")
val someSMS = SMS("123-456-7890", "Hi, are you available for a call?")
println(showNotification(someEmail))
println(showNotification(someSMS))

5>Imperative Quick Sort Algorithm
def quickSortImperative(arr: Array[Int]): Array[Int] = {
  def swap(i: Int, j: Int): Unit = {
    val temp = arr(i)
    arr(i) = arr(j)
    arr(j) = temp
  }
  
  def partition(low: Int, high: Int): Int = {
    val pivot = arr(high)
    var i = low - 1
    for (j <- low until high) {
      if (arr(j) <= pivot) {
        i += 1
        swap(i, j)
      }
    }
    swap(i + 1, high)
    i + 1
  }
  
  def sort(low: Int, high: Int): Unit = {
    if (low < high) {
      val pi = partition(low, high)
      sort(low, pi - 1)
      sort(pi + 1, high)
    }
  }
  
  sort(0, arr.length - 1)
  arr
}

// Example usage:
val arr = Array(10, 7, 8, 9, 1, 5)
println(quickSortImperative(arr).mkString(", "))

6. Write a scala function to convert the each word to capitalize each word 
in the given sentence.
def capitalizeWords(sentence: String): String = {
  sentence.split(" ").map(_.capitalize).mkString(" ")
}

// Example usage:
val sentence = "hello world from scala"
println(capitalizeWords(sentence))

7. Write scala code to show functional style program to implement quick 
sort algorithm.
def quickSortFunctional(arr: List[Int]): List[Int] = {
 if (arr.length <= 1) arr
 else {
 val pivot = arr(arr.length / 2)
 quickSortFunctional(arr.filter(_ < pivot)) ++ arr.filter(_ == pivot) ++ 
quickSortFunctional(arr.filter(_ > pivot))
 }
}
// Example usage:
val list = List(10, 7, 8, 9, 1, 5)
println(quickSortFunctional(list).mkString(", "))

8. For the below given collection of items with item-names and quantity, 
write the scala code for the given statement.
Items = {(“Pen”:20), (“Pencil”:10), (“Erasor”:7), (“Book”:25), 
(“Sheet”:15)}
i. Display item-name and quantity
ii. Display sum of quantity and total number of items
iii. Add 3 Books to the collection
Add new item “Board” with quantity 15 to the collection
val items = List(("Pen", 20), ("Pencil", 10), ("Eraser", 7), ("Book", 25), 
("Sheet", 15))
// i. Display item-name and quantity
items.foreach { case (name, quantity) => println(s"$name: $quantity") }
// ii. Display sum of quantity and total number of items
val totalQuantity = items.map(_._2).sum
val totalItems = items.size
// iii. Add 3 Books to the collection
val updatedItems = items.map {
 case ("Book", quantity) => ("Book", quantity + 3)
 case other => other
}
// Add new item "Board" with quantity 15 to the collection
val finalItems = updatedItems :+ ("Board", 15)
finalItems.foreach { case (name, quantity) => println(s"$name: 
$quantity") }

9. Develop a scala code to search an element in the given list of numbers. 
The function Search() will take two arguments: list of numbers and the 
number to be searched. The function will write True if the number is 
found, False otherwise.
def searchElement(numbers: List[Int], target: Int): Boolean = {
 numbers.contains(target)
}
// Example usage:
val numbers = List(1, 2, 3, 4, 5)
val target = 3
println(searchElement(numbers, target))

10.Illustrate the implementation by writing scala code to generate a down 
counter from 10 to 1.
(10 to 1 by -1).foreach(println)

11.Design a scala function to perform factorial item in the given collection. 
The arguments passed to the function are the collection of items. 
Assume the type of the argument for the function suitably. The return 
type is to be integer.
def factorial(n: Int): Int = {
 if (n <= 1) 1
 else n * factorial(n - 1)
}
// Example usage:
val items = List(2, 3, 4, 5)
val factorials = items.map(factorial)
println(factorials)

12.For the below given collection of items with item names and quantity, 
write the scala code for the given statement. Items = {(“Butter”:20), 
(“Bun”:10), (“Egg”:7), (“Biscuit”:25),(“Bread”:15)}
i. Display item-name and quantity
ii. Display sum of quantity and total number of items
iii. Add 3 Buns to the collection
iv. Add new item “Cheese” with quantity 12 to the collection
val items = Map("Butter" -> 20, "Bun" -> 10, "Egg" -> 7, "Biscuit" -> 25, 
"Bread" -> 15)
// i. Display item-name and quantity
items.foreach { case (name, quantity) => println(s"$name: $quantity") }
// ii. Display sum of quantity and total number of items
val totalQuantity = items.values.sum
val totalItems = items.size
// iii. Add 3 Buns to the collection
val updatedItems = items.updated("Bun", items("Bun") + 3)
// iv. Add new item "Cheese" with quantity 12 to the collection
val finalItems = updatedItems + ("Cheese" -> 12)
finalItems.foreach { case (name, quantity) => println(s"$name: 
$quantity") }


13. Implement function for binary search using recursion in Scala to find 
the number, given a list of numbers. The function will have two 
arguments: Sorted list of numbers and the number to be searched.
def binarySearch(arr: Array[Int], target: Int): Boolean = {
 def search(low: Int, high: Int): Boolean = {
 if (low > high) false
 else {
 val mid = (low + high) / 2
 if (arr(mid) == target) true
 else if (arr(mid) > target) search(low, mid - 1)
 else search(mid + 1, high)
 }
 }
 search(0, arr.length - 1)
}
// Example usage:
val sortedList = Array(1, 2, 3, 4, 5, 6, 7, 8, 9, 10)
val numberToSearch = 5
println(binarySearch(sortedList, numberToSearch))

14. Write a function to find the length of each word and return the word 
with highest length .Ex for the collection of words = (“games”, 
“television”,”rope”,”table”) The function should return 
(“television”,10). The word with the highest length .Read the words 
from the keyboard.
def findLongestWord(words: Array[String]): (String, Int) = {
 words.map(word => (word, word.length)).maxBy(_._2)
}
// Example usage:
val words = Array("games", "television", "rope", "table")
val longestWord = findLongestWord(words)
println(longestWord)
