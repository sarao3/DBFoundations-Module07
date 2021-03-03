*Sara O’Neal*  
*March 1, 2021*  
*Foundations of Databases & SQL Programming (IT FDN 130 A)*  
*Assignment 07*

# SQL Functions

## Introduction
The purpose of this paper is to provide an overview of when to use a SQL User Defined Function (UDF) and explain the differences between Scalar, Inline, and Multi-Statement Functions. To emphasize and illustrate the concepts, I will share examples of the different types of SQL functions.

## When to use a SQL User Defined Function
As we have learned in previous classes, there are several options for storing and reusing query logic within a relational database. One way is to use a SQL Function, which works by passing in a parameter as an input, performs a calculation or combination typically through one or more SQL statements, and returns a result of the calculation or combination based on a pre-defined data type. A programmer can use either built-in database SQL functions (e.g., aggregate functions, data and time functions, etc.) or create their own user-defined functions. When a built-in function does not provide the desired functionality a user is seeking, a custom UDF can be written to their exact requirements to return either a table of values or a single value. The example provided in Figure 1 will return a single value, which in this case is the date and time of the dinner reservation based on a reservation ID used as an input parameter.

![**Figure 1:** A UDF is created that will get the reservation date and time based on a reservation ID.](https://github.com/sarao3/DBFoundations-Module07/blob/main/docs/Figure1.png "**Figure 1:** A UDF is created that will get the reservation date and time based on a reservation ID.")  
**Figure 1:** A UDF is created that will get the reservation date and time based on a reservation ID.

## Differences between Scalar, Inline, and Multi-Statement Functions
There are three different types of SQL User Defined Functions. A Scalar Function will return a single value. An Inline Function contains a single SQL statement and returns a table result set. A Multi-Statement Function contains multiple SQL statements and also returns a table result set. A Multi-Statement Function is similar to Inline Functions with a few differences. The structure of the table that is returned within an Inline Function is determined by the Select statement within the function, however, the structure of the table returned in a Multi-Statement Function is defined. Also, an Inline Function does not have a Begin and End block. An Inline Function often performs better than a Multi-Statement Function. Figure 1 is an example of a Scalar Function because it returns a single value, a date and time. In Figure 2 and 3 below, an example of an Inline Function and Multi-Statement Function are illustrated.

![**Figure 2:** An Inline Function is created by specifying a table as the return type, instead of any scalar data type, and the structure of the table that is returned is determined by the Select statement within the function.](https://github.com/sarao3/DBFoundations-Module07/blob/main/docs/Figure2.png "**Figure 2:** An Inline Function is created by specifying a table as the return type, instead of any scalar data type, and the structure of the table that is returned is determined by the Select statement within the function.")  
**Figure 2:** An Inline Function is created by specifying a table as the return type, instead of any scalar data type, and the structure of the table that is returned is determined by the Select statement within the function.  

![A Multi-Statement Function is created to return a table variable with the structure of the table defined within the function.](https://github.com/sarao3/DBFoundations-Module07/blob/main/docs/Figure3.png "A Multi-Statement Function is created to return a table variable with the structure of the table defined within the function.")  
**Figure 3:** A Multi-Statement Function is created to return a table variable with the structure of the table defined within the function.  

## Summary
When a UDF is used as intended it can be a very powerful tool in a database, especially, when it comes to developing and storing complex and unique query logic not already available as a built-in function. The three types of SQL User Defined Functions are Scalar, Inline, and Multi-Statement.
