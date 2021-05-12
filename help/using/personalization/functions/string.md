---
title: Functions library
description: Functions library
---
# String Functions {#string}

![](../../assets/do-not-localize/badge.png)

Learn how to use String functions in the Expression Editor.

## Camel Case {#camelCase}

The `camelCase` function capitalizes the first letter of each word of a string.

**Format**

```sql
{%= camelCase(string)%}
```

**Example**

The following function will capitalize the first letter of word in the profile's street address.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Concat {#concate}

The `concat` function combines two strings into one.

**Format**

```sql
{%= concat(string,string) %}
```

**Example**

The following function will combine profile city and country in a single string.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Contains {#contains}

The `contains` function is used to determine if a string contains a specified substring.

**Format**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Description |
| --------- | ----------- |
| `STRING_1` | The string to perform the check on. |
| `STRING_2` | The string to search for within the first string. |
| `CASE_SENSITIVE` | An optional parameter to determine if the check is case sensitive. Possible values: true (default) / false. |

**Examples**

* The following function will check if the profile first name contains the letter A (in upper or lower case). If this is the case, it will return 'true', else it will return 'false'.

    ```sql
    {%= contains(profile.person.name.firstName, "A", false) %}
    ```

* The following query determines, with case sensitivity, if the person's email address contains the string "2010@gm".

    ```sql
    {%= contains(profile.person.emailAddress,"2010@gm") %}
    ```

## Does not contain{#doesNotContain}

The `doesNotContain` function is used to determine if a string does not contain a specified substring.

**Format**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Description |
| --------- | ----------- |
| `STRING_1` | The string to perform the check on. |
| `STRING_2` | The string to search for within the first string. |
| `CASE_SENSITIVE` | An optional parameter to determine if the check is case sensitive. Possible values: true (default) / false. |

**Example**

The following query determines, with case sensitivity, if the person's email address does not contain the string "2010@gm".

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## Does not end with{#doesNotEndWith}

The `doesNotEndWith` function is used to determine if a string does not end with a specified substring.

**Format**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | The string to perform the check on. |
| `{STRING_2}` | The string to search for within the first string. |
| `{CASE_SENSITIVE}` | An optional parameter to determine if the check is case sensitive. Possible values: true (default) / false. |

**Example**

The following query determines, with case sensitivity, if the person's email address does not end with ".com".

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Does not start with{#doesNotStartWith}

The `doesNotStartWith` function is used to determine if a string does not start with a specified substring.

**Format**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | The string to perform the check on. |
| `{STRING_2}` | The string to search for within the first string. |
| `{CASE_SENSITIVE}` | An optional parameter to determine if the check is case sensitive. Possible values: true (default) / false. |

**Example**

The following query determines, with case sensitivity, if the person's name does not start with "Joe".

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## Encode 64{#encode64}

The `encode64` function is used to encode or decode a string.

**Format**

```sql
{%= encode64(string) %}
```

## Ends with{#endsWith}

The `endsWith` function is used to determine if a string ends with a specified substring.

**Format**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | The string to perform the check on. |
| `{STRING_2}` | The string to search for within the first string. |
| `{CASE_SENSITIVE}` | An optional parameter to determine if the check is case sensitive. Possible values: true (default) / false.  |

**Example**

The following query determines, with case sensitivity, if the person's email address ends with ".com".

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## Equals{#equals}

The `equals` function is used to determine if a string is equal to the specified string, with case sensitivity.

**Format**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | The string to perform the check on. |
| `{STRING_2}` | The string to compare with the first string. |

**Example**

The following query determines, with case sensitivity, if the person's name is "John".

```sql
{%=equals(profile.person.name,"John") %}

```

## Equals Ignore Case{#equalsIgnoreCase}

The `equalsIgnoreCase` function is used to determine if a string is equal to the specified string, without case sensitivity.

**Format**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | The string to perform the check on. |
| `{STRING_2}` | The string to compare with the first string. |

**Example**

The following query determines, without case sensitivity, if the person's name is "John".

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}

```

## Extract Email Domain {#extractEmailDomain}

The `extractEmailDomain` function is used to extract the domain of an email address.

**Format**

```sql
{%= extractEmailDomain(string) %}
```

**Example**

The following query extracts the email domain of the personal email address.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## Is empty {#isEmpty}

The `isEmpty` function is used to determine of a string is empty.

**Format**

```sql
{%= isEmpty(string) %}
```

**Example**

The following function returns 'true' if the profile's mobile phone number is empty. Else, it will return 'false'.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## Left trim {#leftTrim}

The `leftTrim` function is used to.

**Format**

```sql
{%= leftTrim(string) %}
```

**Example**

The following function .

```sql

```

## Length {#length}

The `length` function is used to get the number of characters in a string or an expression.

**Format**

```sql
{%= length(string) %}
```

**Example**

The following function returns the length of the profile's city name.

```sql
{%= length(profile.homeAddress.city) %}
```

## Like{#like}

The `like` function is used to determine if a string matches a specified pattern.

**Format**

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | The string to perform the check on. |
| `{STRING_2}` | The expression to match against the first string. There are two supported special characters for creating an expression: `%` and `_`. <ul><li>`%` is used to represent zero or more characters.</li><li>`_` is used to represent exactly one character.</li></ul> |

**Example**

The following query retrieves all the cities where profiles live containing the pattern "es".

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## Lower Case{#lower}

The `lowerCase` function converts a string to lower case letters.

**Syntax**

```sql
{%= lowerCase(string) %}
```

**Example**

This function converts the profile first name to lower case letters.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

## Matches{#matches}

The `matches` function is used to determine if a string matches a specific regular expression. Please refer to [this document](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) for more information on matching patterns in regular expressions.

**Format**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Example**

The following query determines, without case sensitivity, if the person's name starts with "John".

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## Not equal to{#notEqualTo}

The `notEqualTo` function is used to determine if a string is not equal to the specified string.

**Format**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | The string to perform the check on. |
| `{STRING_2}` | The string to compare with the first string. |

**Example**

The following query determines, with case sensitivity, if the person's name is not "John".

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## Regular expression group{#regexGroup}

The `Group` function is used to extract specific information, based on the regular expression provided.

**Format**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING}` | The string to perform the check on. |
| `{EXPRESSION}` | The regular expression to match against the first string. |
| `{GROUP}` | Expression group to match against. |

**Example**

The following query is used to extract the domain name from an email address.

```sql
{%= regexGroup(emailAddress,"@(\w+)", 1) %}
```

## Replace {#replace}

The `replace` function is used to.

**Format**

```sql
{%= replace(string,string,string) %}
```

**Example**

The following function .

```sql

```


## Replace All{#replaceAll}

The `replaceAll` function is used to.

**Format**

```sql
{%= replaceAll(string,string,string) %}
```

**Example**

The following function .

```sql

```


## Right trim {#rightTrim}

The `rightTrim` function is used to.

**Format**

```sql
{%= rightTrim(string) %}
```

**Example**

The following function .

```sql

```

## Split {#split}

The `split` function is used to.

**Format**

```sql
{%= split(string,string) %}
```

**Example**

The following function .

```sql

```

## Starts with{#startsWith}

The `startsWith` function is used to determine if a string starts with a specified substring.

**Format**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}

```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | The string to perform the check on. |
| `{STRING_2}` | The string to search for within the first string. |
| `{CASE_SENSITIVE}` | An optional parameter to determine if the check is case sensitive. By default, this is set to true. |

**Example**

The following  query determines, with case sensitivity, if the person's name starts with "Joe".

```sql
{%= startsWith(person.name,"Joe") %}
```

## Title Case{#titleCase}

The **upper** function .

**Syntax**

```sql
{%= titleCase(string) %}
```

**Example**

This function .

```sql

```

## Trim{#trim}

The **trim** function .

**Syntax**

```sql
{%= trim(string) %}
```

**Example**

This function .

```sql

```

## Upper Case{#upper}

The **upperCase** function converts a string to upper case letters.

**Syntax**

```sql
{%= upperCase(string) %}
```

**Example**

This function converts the profile last name to upper case letters.

```sql
{%= upperCase(profile.person.name.lastName) %}
```
