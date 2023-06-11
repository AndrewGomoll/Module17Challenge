# Title
ZIP Code Regex Tutorial

## Summary
This tutotial demonstrates how to use a regex designed to search for ZIP codes and the different functions and technologies used to create this regex.
Here is the regex that will search for the correct formatting for a ZIP code: ^\d{5}(?:[-\s]\d{4})?$

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Author](#author)

## Regex Components

### Anchors
Anchors are static elements which always remain the same. This can be used to check for correct syntax of a string which requires dots, dashes, etc.
In this tutorial, an anchor can be used in one variation of the correct syntax. There are two ways to write a ZIP code. One way is to write a 5 digit string of all numeric values. Another is to write a 5 digit string of numeric values followed by a dash and 4 more numeric characters. If the user enters the second option (more than 5 characters), an anchor can be used to check for a dash between the 5th and 6th element. In the regex used in this tutorial, the section which reads (?:[-/s]\d{4}) is used to check for the 9 digit syntax. The section that reads [-/s] is the anchor that looks for a dash in that section of the string.

### Quantifiers
Quantifiers specify how many of a single type of character to expect in a string. This is used in this example at the points where a curly bracket are used. The first set of curly brackets says to expect 5 digits. The second says to expect 4 digits. The \d at the beginning of both of those brackets says to expect any number 0-9 for each of the 5 or 4 characters expected. 

### Character Classes
Character Classes are a set of metacharacters or types of characters that can be expected just from a key letter that represents the entire character type. In this tutorial, \d is a character class that represents the numbers 0-9. This allows the function to only expect numbers where the character class is called.

### Flags
Flags are also a one character key tag which represents a certain character to be expected. The difference between a flag and a character class is that a flag expects a certain character whereas a character class expects a certain type of character. In this tutorial, the /s flag is used. This flag is put in place to require a dash between the 5th and 6th character. This is different from the anchor elements since the anchor element only expects a dash where the flag expects a break in the string which in this case is a dash.

### Grouping and Capturing
Grouping is a function within the regex function that calls for part of the function to be grouped separately. The grouping function can be initialized by parenthesis. In this tutorial, grouping is used to separate the first 5 numbers from the optional additional 4 numbers. The groups are stored in memory as group 0 being the entire function, and group 1 being the first section within the parenthesis. This allows for 5 digit ZIP codes to still be accepted since in that case, we wouldn't use group 1(the function within the parenthesis) unless there are more digits than the 5 that are expected.

## Author
The author of this tutorial is currently enrolled in the MSU full stack development coding bootcamp.

This is the link to the authors Github: https://github.com/AndrewGomoll