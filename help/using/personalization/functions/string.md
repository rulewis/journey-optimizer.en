---
title: Functions library
description: Functions library
---
# String Functions {#string}

![](../../assets/do-not-localize/badge.png)


TBC CJM String functions

## Like{#like}

The `like` function is used to determine if a string matches a specified pattern.

**Format**

```sql
like ({STRING_1},{STRING_2})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | The string to perform the check on. |
| `{STRING_2}` | The expression to match against the first string. There are two supported special characters for creating an expression: `%` and `_`. <ul><li>`%` is used to represent zero or more characters.</li><li>`_` is used to represent exactly one character.</li></ul> |

**Example**

The following  query retrieves all the cities containing the pattern "es".

```sql
like (city ,"%es%")
```

## Starts with{#startsWith}

The `startsWith` function is used to determine if a string starts with a specified substring.

**Format**

```sql
startsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | The string to perform the check on. |
| `{STRING_2}` | The string to search for within the first string. |
| `{BOOLEAN}` | An optional parameter to determine if the check is case sensitive. By default, this is set to true. |

**Example**

The following  query determines, with case sensitivity, if the person's name starts with "Joe".

```sql
startsWith(person.name,"Joe")
```

## Does not start with{#doesNotStartWith}

The `doesNotStartWith` function is used to determine if a string does not start with a specified substring.

**Format**

```sql
doesNotStartWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | The string to perform the check on. |
| `{STRING_2}` | The string to search for within the first string. |
| `{BOOLEAN}` | An optional parameter to determine if the check is case sensitive. By default, this is set to true. |

**Example**

The following query determines, with case sensitivity, if the person's name does not start with "Joe".

```sql
doesNotStartWith(person.name,"Joe")
```

## Ends with{#endsWith}

The `endsWith` function is used to determine if a string ends with a specified substring.

**Format**

```sql
endsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | The string to perform the check on. |
| `{STRING_2}` | The string to search for within the first string. |
| `{BOOLEAN}` | An optional parameter to determine if the check is case sensitive. By default, this is set to true. |

**Example**

The following query determines, with case sensitivity, if the person's email address ends with ".com".

```sql
endsWith(person.emailAddress,".com")
```

## Does not end with{#doesNotEndWith}

The `doesNotEndWith` function is used to determine if a string does not end with a specified substring.

**Format**

```sql
doesNotEndWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | The string to perform the check on. |
| `{STRING_2}` | The string to search for within the first string. |
| `{BOOLEAN}` | An optional parameter to determine if the check is case sensitive. By default, this is set to true. |

**Example**

The following query determines, with case sensitivity, if the person's email address does not end with ".com".

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Contains{#contains}

The `contains` function is used to determine if a string contains a specified substring.

**Format**

```sql
contains({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | The string to perform the check on. |
| `{STRING_2}` | The string to search for within the first string. |
| `{BOOLEAN}` | An optional parameter to determine if the check is case sensitive. By default, this is set to true. |

**Example**

The following query determines, with case sensitivity, if the person's email address contains the string "2010@gm".

```sql
contains(person.emailAddress,"2010@gm")
```

## Does not contain{#doesNotContain}

The `doesNotContain` function is used to determine if a string does not contain a specified substring.

**Format**

```sql
doesNotContain({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | The string to perform the check on. |
| `{STRING_2}` | The string to search for within the first string. |
| `{BOOLEAN}` | An optional parameter to determine if the check is case sensitive. By default, this is set to true. |

**Example**

The following query determines, with case sensitivity, if the person's email address does not contain the string "2010@gm".

```sql
doesNotContain(person.emailAddress,"2010@gm")
```

## Equals{#equals}

The `equals` function is used to determine if a string is equal to the specified string.

**Format**

```sql
equals({STRING_1},{STRING_2})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | The string to perform the check on. |
| `{STRING_2}` | The string to compare with the first string. |

**Example**

The following query determines, with case sensitivity, if the person's name is "John".

```sql
equals(person.name,"John")
```

## Not equal to{#notEqualTo}

The `notEqualTo` function is used to determine if a string is not equal to the specified string.

**Format**

```sql
notEqualTo({STRING_1},{STRING_2})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | The string to perform the check on. |
| `{STRING_2}` | The string to compare with the first string. |

**Example**

The following query determines, with case sensitivity, if the person's name is not "John".

```sql
notEqualTo(person.name,"John")
```

## Matches{#matches}

The `matches` function is used to determine if a string matches a specific regular expression. Please refer to [this document](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) for more information on matching patterns in regular expressions.

**Format**

```sql
matches({STRING_1},STRING_2})
```

**Example**

The following query determines, without being case sensitive, if the person's name starts with "John".

```sql
matches(person.name.,"(?i)^John")
```

## Regular expression group{#regexGroup}

The `regexGroup` function is used to extract specific information, based on the regular expression provided.

**Format**

```sql
regexGroup({STRING},{EXPRESSION})
```

**Example**

The following query is used to extract the domain name from an email address.

```sql
regexGroup(emailAddress,"@(\w+)", 1)
```


## Functions

## Lower Case{#lower}

The **lowerCase** function converts a string to lower case letters.

Syntax:

```sql
{%=lowerCase(string)%}
```

Example:

This function converts the profile first name to lower case letters.

```sql
{%=lowerCase(profile.person.name.firstName)%}
```

## Upper Case{#upper}

The **upper** function converts a string to lower case letters.

Syntax:

```sql
{%=upperCase(string)%}
```

Example:

This function converts the profile last name to upper case letters.

```sql
{%=upperCase(profile.person.name.lastName)%}
```
