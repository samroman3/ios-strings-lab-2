# Strings Lab 2

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.

## Question 1

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift

var problem = "split this string into words and print them on separate lines"

var problem2 = problem.components(separatedBy: " ")

for i in problem2 {
print (String(i))
}

Example

Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines
```


## Question 2

Given a string `testString` create a new variable called `condensedString` that has any consecutive spaces in `testString` replaced with a single space.

```swift
let testString = "  How   about      thesespaces  ?  "
//condensedString = " How about thesespaces ? "

et condensedString = aString.replacingOccurrences (of: "  ", with: " ", options: .literal, range: nil)
```
l

## Question 3

Given a string with multiple words. Reverse the string word by word.

Example:

Sample Input: `"Swift is the best language"`

Sample Output: `"language best the is Swift"`
```
var question3 = "Swift is the best launguage"

var words = question3.split(separator: " ")

print(words)

for _ in words {
words.reverse()
}
print(words)
```

## Question 4

Given a string with multiple words. Write code that prints how many of them are palindromes.

Example:

Sample Input: `"danaerys dad cat civic bottle"`

Sample Output: `2`

```

var question4 = "danaerys dad cat civic bottle"

var words = question4.split(separator: " ")
var palindromes = 0

for i in words {
if String(i.reversed()) == String(i) {
palindromes += 1
}
}
print(palindromes)
```

## Question 5

You are given a string representing an **attendance record** for a student. The record only contains the following three characters:

`'A' : Absent.`

`'L' : Late.`

`'P' : Present.`

If a student has more than one 'A' or more than 2 continuous 'L's that student should not be rewarded. Print true if student is to be rewarded and False if they shouldn't.

Example:

Sample Input: `"PPALLP"`

Sample Output: `true`
```
let attendance = "PPALLP"
var howManyAs = ""
var howManyLs = "LLL"

for i in attendance{
if i == "A"{
howManyAs += String(i)
}
}
if howManyAs.count > 1 || howManyLs.contains(howManyLs)  {
print (false)
}else {
print (true)
}

```


## Question 6

Given a tuple with two strings. The first string is a **ransom note**, the second string being the characters from a magazine. Determine whether or not you can construct the ransom note using the characters from the magazine.

Each letter from the magazine can only be used once. You can assume all letters are lowercased.

Examples:

Sample Input1: `("a", "b")`

Sample Output1: `False`

Sample Input2: `("aa", "aab")`

Sample Output2: `True`

***
```
var aTuple = ("magazineLetters", "ransomNote")
var aBool = false
var count = 0

for i in aTuple.0 { //h, i
for j in aTuple.1 { //i
if j == i {
count += 1
continue
} else {
continue
}
}
}
if count == (aTuple.0).count {
aBool = true
}

print(aBool)
```
