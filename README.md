# Strings Lab

## Question 2

Given a string testString create a new variable called condensedString that has any consecutive spaces in testString replaced with a single space.


```swift
//Answer: 

let testString = "  How   about      thesespaces  ?  "
let condensedString = testString.split(separator: " ").joined(separator: " ")
print(condensedString)

```



***
## Question 4
Given a string with multiple words. Write code that prints how many of them are palindromes.

Example:

Sample Input: "danaerys dad cat civic bottle"

Sample Output: 2

```swift
let input = "danaerys dad cat civic bottle"
var palindromeCount = 0
for word in input.split(separator: " ") where word == String(word.reversed()) {
palindromeCount += 1
}
print("There were \(palindromeCount) palindromes in the string \"\(input).\"")

```


***
## Question 12

Print the below flower box using the following information.

- The unicode number for ⚘ is U-2698
- The top and bottom of the box are represented by dashes and the rows are |
- Use the terminator argument in your print statements to print on the same line.
- Hint: It may be useful to try printing out a box of just one character to start then work your way from there.

```swift
Flower Box:
- - - - - - - - - - -
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
- - - - - - - - - - -
```
```swift
for _ in 1...10 {
print("\u{2d}", terminator: " ")
}

for _ in 1...5 {
print("\n\u{7c}",terminator: "")
for _ in 1...9 {
print("\u{2698}", terminator: "\u{7c}")
}
}
print("")

for _ in 1...10 {
print("\u{2d}", terminator: " ")
}
```

***
## Question 14

You are given a string stored in the variable `aString`. Create new string named `replacedString` that contains the characters of the original string with all the occurrences of the character `"e"` replaced by `"\*"`.

```swift
var aString = "Replace the letter e with \*"

// Answer: 
var aString = "Replace the letter e with \\*"
var replacedString = aString.replacingOccurrences(of: "e", with: "\\*")
print(aString)
print(replacedString)
 ```

Example:

Input:
`var aString = "Replace the letter e with *"`

Expected values:
`replacedString = "R*plac* th* l*tt*r * with *"`


***
## Question 16

You are given a string stored in variable `aString`. Print `true` if `aString` is a palindrome, and `false` otherwise. A **palindrome** is a string which reads the same backward or forward.

```swift
let aString = "anutforajaroftuna"

// Your code here

//Answer:

let str = "anutforajaroftuna"
let isPalin: Bool

let rvsdStr = String(aString.reversed())

isPalin = aString == rvsdStr

print("It is \(isPalin) that \(str) is a palindrome.")
```

Example 1:
Input:
`var aString = "anutforajaroftuna"`

Output:
`true`

Example 2:
Input:
`var aString = "Hello"`

Output:
`false`


***
## Question 18

You are given a string stored in variable `problem`. Write code that prints the longest word in the string.

```swift
var problem = "find the longest word in the problem description"

// Your code here
//Answer: 

var problem = "split this string into words and print them on separate lines"
var problemSplit = problem.split(separator: " ")
var biggest = ""
for word in problemSplit {
if word.count > biggest.count {
biggest = String(word)
}
}
print(biggest)

```

Example:
Input:
`var problem = "find the longest word in the problem description"`

Output:
`description`

Hint: Keep track of the longest word you encounter and also keep track of its length.


