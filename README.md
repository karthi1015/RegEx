![Image](https://github.com/Brutich/RegEx/blob/master/doc/regexlogo-1.jpg?branch=master)


# Regular expressions in [Dynamo](https://github.com/DynamoDS/Dynamo) #

Regular expressions provide a powerful, flexible, and efficient method for processing text. The extensive pattern-matching notation of regular expressions enables you to quickly parse large amounts of text to find specific character patterns; to validate text to ensure that it matches a predefined pattern (such as an email address); to extract, edit, replace, or delete text substrings; and to add the extracted strings to a collection in order to generate a report. For many applications that deal with strings or that parse large blocks of text, regular expressions are an indispensable tool.
[Regular Expression Language - Quick Reference](https://docs.microsoft.com/en-us/dotnet/standard/base-types/regular-expression-language-quick-reference?view=netframework-4.8)

Regular expressions are now available in Dynamo with this package.

## Regular Expression Examples ##
### Example 1: Replacing Substrings ###
Assume that a mailing list contains names that sometimes include a title (Mr., Mrs., Miss, or Ms.) along with a first and last name. If you do not want to include the titles when you generate envelope labels from the list, you can use a regular expression to remove the titles, as the following example illustrates.
![Image](https://github.com/Brutich/RegEx/blob/master/doc/regex-examples/examples-001.png)
The regular expression pattern ```(Mr\.? |Mrs\.? |Miss |Ms\.? )``` matches any occurrence of "Mr ", "Mr. ", "Mrs ", "Mrs. ", "Miss ", "Ms or "Ms. ". Regex.Replace node replaces the matched string with empty string; in other words, it removes it from the original string.

### Example 2: Identifying Duplicated Words ###
Accidentally duplicating words is a common error that writers make. A regular expression can be used to identify duplicated words, as the following example shows.
![Image](https://github.com/Brutich/RegEx/blob/develop/doc/regex-examples/examples-002.png)
The Regex.Matches method is called with regular expression options set to IgnoreCase. Therefore, the match operation is case-insensitive, and the example identifies the substring "This this" as a duplication.

Note that the input string includes the substring "this? This". However, because of the intervening punctuation mark, it is not identified as a duplication.
