# Optionals lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

`var userName: String?`

Write 3 different ways of safely unwrapping and printing the value of `userName`.  If it is nil, print "No name".

- Method one: Check for nil and force unwrap

- Method two: Optional binding

- Method three: Nil coalescing
```
var userName: String? = "Admin"
//1.
print(userName!)

//2.
userName = "Admin"
if let unwrapUser = userName{
print("This is my username \(unwrapUser)")
}

//3.
var password: Int?
var unwrapPass = password ?? 1234
```

## Question 2

Given optional string `backgroundColor`, write code that safely unwraps and prints it. If backgroundColor is nil, give it a value.

`var backgroundColor: String?`
```
var backGroundColor: String? = "red"
 print(backGroundColor!)
```


## Question 3

Given an optional width and an optional height of a rectangle, write code that calculates and prints the area. Print an error message if either value is nil.

```swift
var width: Double?
var height: Double?
```
```
 var width: Double?
 var height: Double?
 width = 5.0
 height = 10.0

 if let rectangle = width{
     if let area = height{
         print("This is the area \(area * rectangle)")
     }
 }
 else{
     print("Value is nil")
 }
```

## Question 4

Given the following optional variables `name`, `age` and `height`. Write code so that it prints `name`, `age` and `height` if they all have a value. If any are nil, print an error message. Try using optional binding.

```swift
var name: String?
var age: Int?
var height: Double?
```
```
var name: String? = "Tom"
var age: Int? = 20
var height: Double? = 70.0

if let unwrapName = name, let unwrapAge = age, let unwrapHeight = height{
print("My name is \(unwrapName) and I'm \(unwrapAge) years old, also I'm \(unwrapHeight) inches tall")
}
else{
print("Error there is a nil value")
}
```


## Question 5

Given the variables `firstName`, `middleName` and `lastName`. Create a variable called `fullName` that is a nicely formatted string.

```swift
var firstName: String = "Johnny"
var middleName: String?
var lastName: String = "Stone"
```
```
var firstName: String = "Johnny"
var middleName: String?
var lastName: String = "Stone"

if let unwrapName = middleName {
print("no name")
}
else{
print("My full name is \(firstName) \(lastName)")
}
```

## Question 6

Write code that adds 15 to `myIntString`, then prints the sum. Use the `Int()` constructor which returns an optional Int `(Int?)`.

`let myIntString = "35"`

```
var myIntString: String? = "35"
if let unwrapString = myIntString{
if let intString = Int(unwrapString){
print(intString + 15)
}
}
```


## Question 7

Given an optional tuple of optional Ints, write code to safely unwrap the tuple and calculate the sum of its contents that aren't nil.

```swift
var scores: (Int?, Int?, Int?)?

var testCaseOne: (Int?, Int?, Int?)? = (4, nil, 7)
var testCaseTwo: (Int?, Int?, Int?)? = (nil, nil, 9)
var testCaseThree: (Int?, Int?, Int?)? = (5, 10, 24)
```
```
var scores: (Int?, Int?, Int?)?

var testCaseOne: (Int?, Int?, Int?)? = (4, nil, 7)
var testCaseTwo: (Int?, Int?, Int?)? = (nil, nil, 9)
var testCaseThree: (Int?, Int?, Int?)? = (5, 10, 24)
var sum = 0


if let unwrapCaseOne = testCaseOne{
if let s0 = unwrapCaseOne.0{
sum += s0
}
}

if let unwrapCaseOne = testCaseOne{
if let s1 = unwrapCaseOne.1{
sum += s1
}
}

if let unwrapCaseOne = testCaseOne{
if let s2 = unwrapCaseOne.2{
sum += s2
}
}
print(sum)
```

## Question 8

Safely unwrap `tuple` if there’s a non-nil tuple value and print it out.

```swift
var tuple: (Int, Int)?
if Bool.random() {
 tuple = (5, 3)
}
```
```
var tuple: (Int, Int)?
if Bool.random() {
tuple = (5, 3)
}

if let unwrapT = tuple{
print(unwrapT)
}
else{
print("there is nil value")
}
```


## Question 9

Write code that either doubles `myInt` and then prints it, or prints an error message if myInt is nil.

```swift
var myInt: Int?
if Bool.random() {
 myInt = 5
}
```
```
var myInt: Int?
if Bool.random() {
myInt = 5
}
if let unwrapInt = myInt{
print(unwrapInt * 2)
}
else{
print("Bool is false / nil")
}
```


## Question 10

Write code that prints out the product of `myDouble` and `doubleTwo` or prints an error message if `myDouble` is nil.

```swift
var myDouble: Double?
let doubleTwo: Double = 5

if Bool.random() {
 myDouble = 12
}
```
```
var myDouble: Double?
let doubleTwo: Double = 5

if Bool.random() {
myDouble = 12
}

if let unwrapDouble = myDouble {
print(unwrapDouble * doubleTwo)
}
else{
print("myDouble is nil")
}
```


## Question 11

Determine if the variable contains a Boolean or nil value. If nil set the variable to false, else keep it true.

```swift
var isTheGreatest: Bool?

if Bool.random() {
 isTheGreatest = true
}
```
```
var isTheGreatest: Bool?

if Bool.random() {
isTheGreatest = true
}

if let unwrapBool = isTheGreatest{
print("The variable is \(unwrapBool)")
}
else{
var unwrapGreatest = isTheGreatest ?? (false)
print("The variable is \(unwrapGreatest)")
}
```


## Question 12

Given the code below print the sum of each non-nil element in `myTuple`.

 ```swift
var myTuple: (Int?, Int?, Int?, Int?)

if Bool.random() {
 myTuple.0 = 5
 myTuple.2 = 14
} else {
 myTuple.1 = 9
 myTuple.3 = 10
}
```
```
var myTuple: (Int?, Int?, Int?, Int?)
var sum = 0

if Bool.random() {
myTuple.0 = 5
myTuple.2 = 14
} else {
myTuple.1 = 9
myTuple.3 = 10
}

if let t0 = myTuple.0{
sum += t0
}
if let t1 = myTuple.1{
sum += t1
}
if let t2 = myTuple.2{
sum += t2
}
if let t3 = myTuple.3{
sum += t3
}
print(sum)
```


## Question 13

Given the helper functions and code below, check to see if your `evolutionaryStone` is able to evolve your pokemon.  The table below shows the appropriate matches of pokemon to stone:

| Pokemon	   | Stone    |
| :--------: | :------: |
| Pikachu	   | Electric |
| Bulbasaur	 | Grass    |
| Charmander | Fire     |
| Squirtle	 | Water    |


```swift
// Helper Functions

func eStone() -> String {
 let random = Int(arc4random_uniform(5))
 switch random {
 case 0:
  return "Electric"
 case 1:
  return "Grass"
 case 2:
  return "Fire"
 case 3:
  return "Water"
 default:
  return "No Stone"
 }
}

func starterPokemon() -> String {
 let random = Int(arc4random_uniform(5))
 switch random {
 case 0:
  return "Pikachu"
 case 1:
  return "Bulbasaur"
 case 2:
  return "Charmander"
 case 3:
  return "Squirtle"
 default:
  return "Not a Pokemon"
 }
}

let pokemon: String?
var evolutionaryStone: String?
pokemon = starterPokemon()
evolutionaryStone = eStone()
```
```
let number = Int.random(in: 0 ..< 4)
let number2 = Int.random(in: 0 ..< 4)

func eStone() -> String {
let random = Int(number)
switch random {
case 0:
return "Electric"
case 1:
return "Grass"
case 2:
return "Fire"
case 3:
return "Water"
default:
return "No Stone"
}
}

func starterPokemon() -> String {
let random = Int(number2)
switch random {
case 0:
return "Pikachu"
case 1:
return "Bulbasaur"
case 2:
return "Charmander"
case 3:
return "Squirtle"
default:
return "Not a Pokemon"
}
}

let pokemon: String?
var evolutionaryStone: String?
pokemon = starterPokemon()
evolutionaryStone = eStone()

if let unwrapPokemon = pokemon{
if let unwrapStone = evolutionaryStone{
if unwrapPokemon == "Pikachu"{
if unwrapStone == "Electric"{
print("Pikachu Evolves")    
}
else{
print("Wrong Stone for Pikachu")
}
}
else if unwrapPokemon == "Bulbasaur"{
if unwrapStone == "Grass"{
print("Bulbasaur Evolves")
}
else{
print("Wrong Stone for Bulbasaur")
}
}
else if unwrapPokemon == "Charmander"{
if unwrapStone == "Fire"{
print("Charmander Evolves")
}
else{
print("Wrong Stone for Charmander")
}
}
else if unwrapPokemon == "Squirtle"{
if unwrapStone == "Water"{
print("Squirtle Evolves")
}
else{
print("Wrong Stone for Squirtle")
}
}
else{
print("Not a pokemon")
}
}
}
```


## Question 14

Given an optional int `numberOfPeople`, write code that unwraps and prints it **only if it is even**. Try using optional binding with a condition.

```swift
var numberOfPeople: Int?

if Bool.random() {
 numberOfPeople = 108
}
```
```
var numberOfPeople: Int?

if Bool.random() {
numberOfPeople = 108
}

if let unwrapPeople = numberOfPeople{
if unwrapPeople % 2 == 0{
print("There are this amount \(unwrapPeople) of people")
}
else{
print("There is no people")
}

}
else{
print("The value is nil")
}
```


## Question 15

Given the array of optional Ints `someNumbers`, write code to find the product of the array not including any nil values.

```swift
var someNumbers: [Int?] = []

for i in 0..<20 {
    someNumbers.append(Bool.random() ? i : nil)
}
```
```
var someNumbers: [Int?] = []
var num = 1

for i in 1..<20 {
someNumbers.append(Bool.random() ? i : nil)
}

for i in someNumbers{
if let unwrapNumbers = i{
num = num * unwrapNumbers
}
}
print("The product of someNumbers:\(num)")
```


## Question 16

Given the array `poorlyFormattedCityNames`, create a new array with the city names capitalized and any nil values removed.

```swift
let poorlyFormattedCityNames: [String?] = ["new york", "BOSTON", nil, "chicago", nil, "los angeles", nil, "Dallas",]

Output: ["New York", "Boston", "Chicago", "Los Angeles", "Dallas"]
```
```
let poorlyFormattedCityNames: [String?] = ["new york", " boston", nil, " chicago", nil, " los angeles", nil, " Dallas",]
var string = ""

for i in poorlyFormattedCityNames{
if let unwrapPoorly = i{
//string += unwrapPoorly
//print(unwrapPoorly.capitalized)
}
}
//print(string)
```

## Question 17

Given a random array of optional numbers, create a new array of all the even numbers that aren't nil.

```swift
var aBunchOfNumbers: [Int?] = []

for _ in 0..<20 {
 aBunchOfNumbers.append(Bool.random() ? Int(arc4random_uniform(102)) : nil)
}
```
```
var aBunchOfNumbers: [Int?] = []
var newArray: [Int] = []

for _ in 0..<20 {
aBunchOfNumbers.append(Bool.random() ? Int(Int.random(in: 0 ..< 102)) : nil)
}
//print(aBunchOfNumbers)
for i in aBunchOfNumbers{
if let unwrapBunch = i {
if unwrapBunch % 2 == 0{
newArray.append(unwrapBunch)
}
} 
}
print(newArray)
```


## Question 18

Given the following array of zip codes as strings, write code that turns them into an array of Ints.

`let zipCodeStrings = ["11377", "11101", "11373", "10014", "10003", "11223"]`
```
let zipCodeStrings = ["11377", "11101", "11373", "10014", "10003", "11223"]

for i in zipCodeStrings{
if let integerVersion = Int(i){
print(integerVersion)
}
}
```

## Question 19

Some students were asked some questions about their favorite foods and colors and the answers were stored in an array `studentInfo`.

- Print the names of the students that do not have a favorite color.

- Print the names of the students that don't have a favorite color or a favorite food.

- Create a new array of type `[(String, String, String)]` that contains the students with both favorite colors and foods.

`let studentInfo: [(String, String?, String?)] = [("Bill", "Burgers", "Blue"), ("Rita", nil, "Red"), ("Peter", "Pizza", "Purple"), ("Sarah", "Sandwiches", nil), ("Jeff", nil, nil), ("Lucy", "Leftovers", "Lilac"), ("Mike", "Meat", "Mauve"), ("Gemma", nil, "Green")]`

```
var studentData: [(String?, String?, String?)] = []

let studentInfo: [(String, String?, String?)] = [("Bill", "Burgers", "Blue"), ("Rita", nil, "Red"), ("Peter", "Pizza", "Purple"), ("Sarah", "Sandwiches", nil), ("Jeff", nil, nil), ("Lucy", "Leftovers", "Lilac"), ("Mike", "Meat", "Mauve"), ("Gemma", nil, "Green")]

var noFaves = [String]()
var noFavesColor = [String]()
var faves = [String]()

for info in studentInfo{
if info.1 != nil && info.2 != nil {
faves.append(info.0)
}
if info.2 == nil{
noFavesColor.append(info.0)
}
if info.1 == nil && info.2 == nil {
noFaves.append(info.0)
}
}
print(noFavesColor)
print(noFaves)
print(faves)
```


## Question 20

Given an optional array of optional tuples of optional UInt8s,

- Write code to safely unwrap and print the tuples in the array with all 3 RGB values.

- Write code that counts all the nil values.

`let possibleColors: [(r: UInt8?, g: UInt8?, b: UInt8?)?]? = [(128, 21, 7), (0, 0, 0), nil, (nil, 25, 82), (255, 255, 255), nil, (200, 100, nil), (120, nil, 23), (0, 255, 106), (nil, nil, nil), nil, (100, 100, 200)]`


## Question 21

Consider the following nested optional. It corresponds to a number inside a box inside a box inside a box.

- Fully force unwrap and print number.

- Optionally bind and print number.

`let number: Int??? = 10`
```
let number: Int??? = 10

//print(number!!!)
if let unwrapNum = number{
if let unwrapAgain = unwrapNum{
if let unwrapLast = unwrapAgain{
print(unwrapLast)
}
}
}
```


## Question 22

Given an Array of Optional Strings, write code that concatenates all non-nil values together except for strings with 3 or more vowels.

`let monkeyingAround = ["orangutan", "apes",nil, "monkeys", "gorillas", "lemurs", nil]`

output: `"apesmonkeyslemurs"`
```
//not quite finished

let monkeyingAround = ["orangutan", "apes",nil, "monkeys", "gorillas", "lemurs", nil]


var vowels = "aeiou"
var index = 0
var index1 = 0
var stuff: [String] = []
var empty = ""

for i in monkeyingAround{
if let unwrapMonkey = i{
stuff.append("\(unwrapMonkey)")
}
}

for x in stuff{
for y in stuff[index]{
//print(y)
if vowels.contains(y){
continue
}
empty.append(stuff[index])
}
index += 1
}
print(empty)
if stuff[index].count >= 3{

}

```


## Question 23

Given the value below, print out all of the non-nil Ints it contains by accessing each of them.

`var strangeStructure: ([Int]?, [[Int?]], [[Int]?], Int)? = ([1], [[2,3,4],[],[5,nil],[nil]], [nil, [6,7,8],nil,[],[9]], 10)`
