---
title: Helper functions library
description: Journey Optimizer Helper functions library
---

# Templating language and helper functions {#functionsL}

![](../../assets/do-not-localize/badge.png)


## About templating language

Use Journey Optimizer templating language to perform operations on data, such as calculations, data formatting or conversions, conditions, and manipulate them in the context of personalization.

Templating language is leveraged in helper functions available in personalization drop-down list of the Expression Editor, as below:

![](../assets/access-helper-functions.png)

They are grouped into three categories: [Functions](#functions-helper), [Helpers](#helper-helper) and [Operators](#operators-helper).

### Functions{#functions-helper}

**Array Functions**
 
<table>
    <tr>
        <td><a href="aggregation.md#average">Average</a> (average)</td><td>This function returns the arithmetic mean of all the selected values within the array</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">In</a> (in)</td><td>This function is used to determine if an item is a member of an array or list</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">Minimum</a> (min)</td><td>This function returns the smallest of all the selected values within the array</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">Count</a> (count)</td><td>This function returns the number of elements within the given array</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">Includes</a> (includes)</td><td>This function determines if an array or list contains a given item</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">Not in</a> (notIn)</td><td>This function determines if an item is not a member of an array or list</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">Distinct</a> (distinct)</td><td>This function gets values from an array or list with duplicate values removed</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">Intersects</a> (intersects)</td><td>This function determines if two arrays or lists have at least one common member</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">Subset of</a> (subsetOf)</td><td>This function determines if a specific array (array A) is a subset of another array (array B), i.e. if all elements in array A are elements of array B</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">First item</a> (head)</td><td>This function returns the first item in the array or list</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">Last n in array</a> (lastN)</td><td>This function returns the last `N` items in an array, when sorted in ascending order based on the given numerical expression</td>
    </tr>
    <tr>
        <td>Sum</td><td>TBD</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">First n in array</a> (topN)</td><td>This function returns the first `N` items in an array, when sorted in ascending order based on the given numerical expression</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">Maximum</a> (max)</td><td>This function returns the largest of all the selected values within the array</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">Superset of</a> (supersetOf)</td><td>This function termines if a specific array (array A) is a superset of another array (array B), i.e. if that array A contains all elements in array B</td>
    </tr>
</table>


**Map Functions**

<table>
    <tr>
        <td><a href="maps.md#get">Get</a> (get)</td><td>This function is used to retrieve the value of a map for a given key</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">Keys</a> (keys)</td><td>This function is used to retrieve all the keys for a given map</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">Values</a> (values)</td><td>This function retrieves all the values of a given map</td>
    </tr>
</table>

**Object Functions**

<table>
    <tr>
        <td><a href="objects.md#isNotNull">Is not null</a> (isNotNull)</td><td>This function is used to determine if an object reference exists</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">Is null</a> (isNull)</td><td>This function is used to determine if an object reference does not exist</td>
    </tr>
</table>

**String Functions**

<table>
    <tr>
        <td><a href="string.md#camelCase">Camel Case</a> (camelCase)</td><td>This function is used to capitalize the first letter of each word of a string</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">Concat</a> (Concat)</td><td>This function is used to combine two strings into one</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">Contains</a> (contains)</td><td>This function is used to determine if a string contains a specified substring</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">Does not contain</a> (doesNotContain)</td><td>This function is used to determine if a string does not contain a specified substring</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">Does not end with</a> (doesNotEndWith)</td><td>This function is used to determine if a string does not end with a specified substring</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">Does not start with</a> (doesNotStartWith)</td><td>This function is used to determine if a string does not start with a specified substring</td>
    </tr>
    <tr>
        <td><a href="string.md#encode64">Encode 64</a> (encode64)</td><td>This function is used to encode or decode a string</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">Ends with</a> (endsWith)</td><td>This function is used to determine if a string ends with a specified substring</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">Equals</a> (equals)</td><td>This function is used to determine if a string does not start with a specified substring, with case sensitivity</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">Equals Ignore Case</a> (equalsIgnoreCase)</td><td>This function is used to determine if a string does not start with a specified substring, without case sensitivity</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">Extract Email Domain</a> (extractEmailDomain)</td><td>This function is used to extract the domain of an email address</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">IsEmpty</a> (isEmpty)</td><td>This function is used to check if a string or expression is empty.</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">Left trim</a>(leftTrim)</td><td>TBD</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Length</a> ()</td><td>This function is used to get the number of characters in a string or an expression</td>
    </tr>
    <tr>
        <td><a href="string.md#like">Like</a> (like)</td><td>This function is used to determine if a string matches a specified pattern</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">Lower Case</a> (lowerCase)</td><td>This function converts a string to lower case letters</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">Matches</a> (matches)</td><td>This function is used to determine if a string matches a specific regular expression</td>
    </tr>
    <tr>
        <td><a href="string.md#like">MD5</a> ()</td><td>TBD</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">Not equal to</a> (notEqualsTo)</td><td>This function is used to determine if a string is not equal to the specified string</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">Regular expression group</a> (regexGroup)</td><td>This function is used to extract specific information, based on the regular expression provided</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Replace</a> (replace)</td><td>TBD </td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">Replace all</a> (replaceAll)</td><td>TBD</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">Right trim</a>(rightTrim)</td><td>TBD </td>
    </tr>
    <tr>
        <td><a href="string.md#split">Split</a> (split)</td><td>TBD</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">Starts with</a> (startsWith)</td><td>This function is used to determine if a string starts with a specified substring</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">Title Case</a> (titleCase)</td><td>TBD</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">Trim</a> (trim)</td><td>TBD</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">Upper case</a> (upperCase)</td><td>This function converts a string to upper case letters</td>
    </tr>
</table>

### Helpers{#helper-helper}

Helpers are detailed in [this page](../personalization-syntax.md#helpers-all).

Available helpers are:

* Each - [Learn more](../personalization-syntax.md#each)
* If  - [Learn more](../personalization-syntax.md#if)
* Let - [Learn more](../personalization-syntax.md#let)
* Unless  - [Learn more](../personalization-syntax.md#unless)
* With  - [Learn more](../personalization-syntax.md#with)

### Operators{#operators-helper}

These operators can only be used with numbers.

<table>
    <tr>
        <td><a href="operators.md#add">Addition</a> ('+')</td><td>This operator adds two numbers</td>
    </tr>
    <tr>
        <td><a href="operators.md#and">And</a> (and)</td><td>This operator creates a logical conjunction</td>
    <tr>
        <td><a href="operators.md#divide">Divide</a> (/)</td><td>This operator is used to find the quotient of two numbers</td>
    </tr>
    <tr>
        <td><a href="operators.md#and">Equals to</a> (=)</td><td>This operation checks if values are equal</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Greater than</a> ()</td><td>This operator checks if first value is greater than the second value</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Greater or equals to</a> (=>)</td><td>This operator checks if first value is greater than or equal to the second value</td>
    </tr>
    <tr>
        <td><a href="operators.md#multiply">Multiplication</a> (*)</td><td>This operator multiplies two numbers</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">Negation</a> (!)</td><td>This operator creates a logical negation</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">Not equals to</a> (=!)</td><td>This operator checks if given expression not equal to give value</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">Or</a> (or)</td><td>This operator creates a logical disjunction</td>
    </tr>
    <tr>
        <td><a href="operators.md#remainder">Remainder</a> (%)</td><td>This operator is used to calculate the remaindes after dividing two numbers</td>
    </tr>
    <tr>
        <td><a href="operators.md#remainder">Smaller than</a> ()</td><td>This operator checks if first value is less than the second value</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">Smaller or equals to</a> ()</td><td>This operator checks if first value is smaller than or equal to the second value</td>
    </tr>
    <tr>
        <td><a href="operators.md#substract">Substraction</a> ()</td><td>This operator substracts two numbers</td>
    </tr>
</table>
