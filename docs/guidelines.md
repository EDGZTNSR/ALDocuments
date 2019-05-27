# Guidelines for AL Development!

## Filenaming Notation
 Files need to be written in the following syntax : 
>````"<Type><Id>.<ObjectName>.al````
>>Example : Cod50100.TestCodeunit.al
>>Example : Pag21.CustomerCard.al

## Type Map
|Object                |Abbrevation                |
|------------------|-------------------------------|
|Page			   |`'Pag'`     |
|Page Extension    |`'PagExt'`  |
|Page Customization|`'PagCust'` |
|Codeunit          |`'Cod'`     |
|Table             |`'Tab'`     |
|Table Extension   |`'TabExt'` 	|
|XML Port          |`'Xml'`     |
|Report            |`'Rep'`     |
|Query             |`'Que'`     |
|Enum              |`'Enu'`     |
|Enum Extension	   |`'EnuExt'`  |
|Control Add-ins   |`'ConAddin'`|

## Formatting

 - Use all lowercase letter for keywords.
 - Use spaces for indentation
 - Curly brackets are always on a new line
```
page 123 PageName
{
    actions
    {
        area(Processing)
        {
            action(ActionName)
            {
                trigger OnAction()
                begin
                end;
            }
        }
    }
}
```
## Line lenght

There is no restrection but to prevent unreadable Code keept your lines to a maximum of **79 characters**.

## Object Naming

Object names are **prefixed**. They start with a feature/group name, followed by the locical name.

## File structure
Inside the ```.al``` code file, the structure for all objects must be followed by the sequence below.
 1. Properties
 2. Object-specific constructs as:
	 - Table fields
	 - Page Layout
	 - Actions
3.	Global variables
	- Labels
	- Global variables
4.	Methods
 
## Referencing
In AL, objects are **referenced by** their **name**, not their ID!!!

## Variable naming
Variables must:
 - Be named using PascalCase
 - have the ``_l`` suffix if they are local
 - have the ``_g`` suffix if they are global
 - have the ``_p`` suffix if they are a parameter
 - not have empty spaces in the variable name
 
 Exception for Counter Variables like ``i``.
 
## Method declaration
To declare a method, follow the guidelines below:

 - include a space after a semicolon when declaring multiple arguments
    >local procedure MyProcedure(Customer: Record Customer; Int: Integer)
- Methods are named in PascalCase
- Methods with return values start with "Get" and the discription of the return value

## Calling Methods

When calling a method, follow the guidelines below:

 - Include one space after each argument when calling with multiple.
 - Parantheses must be specified.


## Field numbering
When creating new Tables, following should be considered:

 - fields for the primary key are generated with the fieldnumbers from 1 to 9.
 - all other fields should start with the fieldnumber 10
 - keep practical grouping in mind so more fields could be added later

## Strings and other literals
When working with Strings or other literals please follow the guides below:

- Stings, numbers, etc. are not directly coded (not hardcoded)
- Translations are written only in German (DES) or English (ENU) other languages only on customer request
