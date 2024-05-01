# Coding Guidelines for Qlik View Project

This document outlines the coding guidelines to be followed while writing code for the project.

## Table of Contents

1. [Naming Conventions](#1-naming-conventions)
2. [Indentation](#2-indentation)
3. [Comments](#3-comments)

## General Guidelines

- **Use meaningful names**: Use meaningful names for variables, functions, and subroutines. This makes the code more readable and understandable.
- **Use comments**: Use comments to explain the code. Comments should be used to explain the purpose of the code, the logic behind it, and any assumptions made.
- **Use whitespace**: Use whitespace to make the code more readable. Use spaces to separate operators and operands, and to indent the code.
- **Use consistent formatting**: Use consistent formatting throughout the code. This makes the code more readable and maintainable.
- **Use version control**: Use version control to track changes to the code. This makes it easier to collaborate with others and to revert to previous versions of the code if needed.
- **Use error handling**: Use error handling to handle exceptions and errors. This makes the code more robust and prevents it from crashing.
- Avoid using numbers and vague terms like data or info in names. Instead, use names that reflect the purpose, like customerEmail or calculateTotal.

## 1. Naming Conventions

### 1.1 Camel Case, Pascal Case, Snake Case

### 1.1.1 Camel Case

Camel case is the practice of capitalizing the first letter of each word in a series and then removing spaces, numbers, underscores, hyphens, and other special characters.

### Basic Camel Case Capitalization Rules

- The first letter is capitalized.
- One or more letters in that word are also capitalised.
- The word does not end on a capitalized letter: CamelCasE
- No two capitalised letters shall follow directly each other: CamelCAse
- No number in that word at any place: CamelCase1more
No dot(.), under_score or dash (-) within the word, only letters: Camel_Case
- No ‘foreign’ letters in it like äöüß or accentuated like áéí. CämélCáße

### 1.1.2 Pascal Case

Pascal case is similar to camel case, but the first letter of the first word is also capitalized.

### Examples of camel case and Pascal case

#### Upper Camel Case (Pascal Case)

- ThisIsAnExampleOfTheUpperCamelCaseForm
- TheFirstLetterIsCapitalizedAndEachWordThroughoutIsAsWell

#### Lower Camel Case

- theFirstLetterIsNotCapitalizedAndEachWordThroughoutIs
- thereAreNoHyphensOrSpacesInThisCamelCase

### 1.1.3 Snake Case

#### Basic Snake Case Capitalization Rules

- All letters are lowercase.
- All spaces between words are filled with underscores.
- Remove all punctuation.

### Examples of snake case

- “This is a sample sentence” turns into “this_is_a_sample_sentece”
- “I love using snake case when I’m writing code”  turns into “i_love_using_snake_case_when_im_writing_code”

---

### 1.2 Naming Conventions for Different Types of Entities

- **Variables**: Use camelCase for variable names. Variable names should be descriptive and meaningful. Examples:

    ```csharp
    Set vCustomerName = 'John Doe';
    Let vTotalSales = 10000;
    Let vYesterday=8/25/2014-1;
    ```

- **Constants**: Use all uppercase letters with underscores to separate words.
- **Functions**: Use camelCase for function names. Function names should be descriptive and meaningful.

- **Subroutines**: Use Use PascalCase (also known as UpperCamelCase) for subroutine names. Subroutine names should be descriptive and meaningful. Examples:

    ```csharp
    Sub StoreAndDrop(vTableName)
        Store [$(vTableName)] into [$(vQVDPath)\$(vTableName).qvd];
        Drop Table [$(vTableName)];
    End Sub
    
    Call StoreAndDrop('TableName');
    ```

- **Tables**: Use PascalCase (also known as UpperCamelCase) for table names. Table names should be descriptive and meaningful. Examples:

    ```sql
    Customers
    OrderDetails
    ProductCategories
    EmployeeAddresses
    ```

- **Fields**: Use camelCase for field names. Field names should be descriptive and meaningful. Examples:

    ```sql
    ProductId
    CustomerName
    OrderDate
    ProductCategory
    EmployeeAddress
    ```

### 1.3 References

- https://capitalizemytitle.com/camel-case/

## 2. Indentation

- Indentation should be consistent throughout the code.
- Use 4 spaces for indentation.
- Use spaces to separate operators and operands.
- Use blank lines to separate blocks of code.
- Use indentation to make the code more readable and understandable.
- Example:

    ```csharp
    Sub MissingValues
        For Each vField In Fields
            If IsNull(vField) Then
                vField = 0;
            End If;
        Next vField;
    End Sub

    If vTotalSales > 10000 Then
        Let vBonus = vTotalSales * 0.1;
    Else
        Let vBonus = vTotalSales * 0.05;
    End If;
    ```

## 3. Comments

- Use comments to explain the code.
- Comments should be used to explain the purpose of the code, the logic behind it, and any assumptions made.
- Comments should be concise and to the point.
- Avoid using comments to explain obvious code.
- Use comments to explain complex or non-obvious code.
- Use comments to explain the purpose of variables, functions, and subroutines.
