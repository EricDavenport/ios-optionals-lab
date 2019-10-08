# Optionals lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

a. Given the variable `userNameOne` below, print *"The username is Test User"*.  Use *Optional Binding* (`if let`) to print the name.

```swift
var userNameOne: String? = "Test User"

if let userName = userNameOne {
print("The username is \(userName)")
}
```

b. Given the variable `userNameTwo` below, print *"The username is undefined"*.  Use the *nil coalescing operator* (`??`).

```swift
var userNameTwo: String? = nil
print(userNameTwo ?? "Undefined")
```

## Question 2

a. Given the variables `rectOneWidth` and `rectOneHeight` below, print "The area of rectOne is 50".  Use *Optional Binding* (`if let`) to print the area.

```swift
var rectOneWidth: Double? = 5
var rectOneHeight: Double? = 10
var rectOneArea: Double

if let rectWidth = rectOneWidth {
    if let rectHeight = rectOneHeight {
        rectOneArea = (rectWidth * rectHeight)
    print("The area of rectOne is \(rectOneArea)")
    }
}

```

b. Given the variables `rectTwoWidth` and `rectTwoHeight` below, print "The area of rectTwo is not able to be calculated".  Use *Optional Binding* (`if let`) to print this message.

```swift
var rectTwoWidth: Double? = nil
var rectTwoHeight: Double? = nil
var rectTwoArea: Double

if let rect2Width = rectTwoWidth,
    let rect2Height = rectTwoHeight {
    rectTwoArea = rect2Width * rect2Height
    print("The area of rectTwo is \(rectTwoArea)")
} else {
    print("The area of the rectTwo is not able to be calculated.")
}
```

## Question 3

a. Given the variables `userOneName`, `userOneAge`, and `userOneHeight` below, write code that prints "Hello Anne!  You are 15 years old and 5.8 feet tall" (1 foot = 12 inches).  Use optional binding.


```swift
var userOneName: String? = "Anne"
var userOneAge: Int? = 15
var userOneHeight: Double? = 70

if let user1Name = userOneName {
    if let user1Age = userOneAge {
        if let user1Height = userOneHeight {
            print("Hello \(user1Name)! You are \(user1Age) years old and \(user1Height) feet tall")
        }
    }
}
```

b. Given the variables `userTwoName`, `userTwoAge` and `userTwoHeight` below, write code that prints "Hello user!  You are 15 years old and I don't know how tall you are".  Use optional binding

```swift
var userTwoName: String? = nil
var userTwoAge: Int? = 15
var userTwoHeight: Double? = nil

if let user2Name = userTwoName,
let user2Age = userTwoAge,
let user2Height = userTwoHeight {
    print("Hello \(user2Name)! You are \(user2Age) years old and \(user2Height) feet tall")
} else {
    print("Hello User, you are \(userTwoAge ?? 8) years old and I dont know how tall you are.")
}
```


## Question 4

Give the variable `favoriteNumber`, write code that either prints "Your favorite number is " followed by the number, or "I don't know what your favorite number is"

`favoriteNumber` is of type Int? and will either be `nil` or a random number between 0 and 10.  It will change each time you run your Playground.

```swift
var favoriteNumber = Bool.random() ? Int.random(in: 0...10) : nil

if let num = favoriteNumber {
    print("Your favorite number s \(num)")
} else {
    print("I don't know your favorite number.")
}
```



## Question 5

Given the variables `numOne`, `numTwo` and `numThree`, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift

var numOne = Bool.random() ? Int.random(in: 0...10) : nil
var numTwo = Bool.random() ? Int.random(in: 0...10) : nil
var numThree = Bool.random() ? Int.random(in: 0...10) : nil
var sum: Int

if let num1 = numOne, let num2 = numTwo, let num3 = numThree {
    let sum = num1 + num2 + num3
    print(sum)
    print("The sum of all the numbers is \(sum)")
    if sum == 0 {
         print(sum)
         print("The sum of all the numbers is \(sum)")
    }
}

//there are print statements before both prints(the sum of...) print statements were so i coul confirm the sum niul or not - for peronal use
```

## Question 6

a. Given the variable `numbers` below, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift
var numbers = [Int?]()

for _ in 0..<10 {
    numbers.append(Bool.random() ? Int.random(in: 0...100) : nil)
}
```

b. Using the same variable, find the average of all non-nil values.

## Extra Questions

https://github.com/joinpursuit/Pursuit-Core-iOS-Extra-Optionals-Questions/blob/master/README.md
