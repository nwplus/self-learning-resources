# Database Basics

Consider all the organizations you've registered with in your lifetime. They probably range from non-essential services like Facebook and Reddit, to much more important ones such as banking and education. Regardless of what you signed up for, it's a guarantee that your personal information has been stored by the company somewhere. And it doesn't just stop with registration data. Sports teams keep track of player statistics, shops record daily transactions, there are infinite applications of the kinds of data we might be interested in saving for future access and analysis. As you might have guessed, the most effective storage medium used to accomplish this are **databases**.

<br>

## What is a database?
At its core, a database is simply an **organized collection of data**. It may come as a surprise, but databases don't need to be stored on hardware to be classifised as one. Physical paper-based databases are definitely a thing and were much more common in the past (e.g. phonebooks, ledgers). What really defines a database is the fact that the data is kept in a **organized** manner, and not just scribbled down without any structure. 

- png of unogranized data (email or sth)
- png of organized data (table)

But let's think for a moment. Could something like an Excel spreadsheet be considered a database? Using a spreadsheet, you could certainly organize data in a structured tabular format.

- png of excel spreadsheet

Seems pretty organized to me! Going by our original definition, you could definitely label a spreadsheet as a database. However, we are tech folk! When we talk and think about databases, we probably aren't visualizing Excel or Google Sheets. The databases we mull over are a lot more than just simple data containers. They should support efficient queries. They should keep the data clean. They should be secure. All these critical features aren't available with databases alone. We need to include an extra piece in our database mental model that isn't mentioned nearly as often: **Database Management Systems**. 

<br>

## Database Management Systems (DBMS)

On its own, databases aren't actually.   A DBMS is a type of software that allows users to manage a database. the 



## Why do we need databases?
Databases are more than just storage containers for data. If that's all they were capable of, there would be little reason to choose a database over something like a spreadsheet. However, databases were designed to solve important data collection and maintenance issues that traditional storage mediums don't always address. Here are some of the main reasons we love databases:

### Efficient Storage
Databases are able to store an enormous number of records in very little space. Unlike spreadsheets, databases do not have record limitations.

### Data Integrity
Data integrity describes the accuracy and consistency of your data. One of the most prevalent issues with using spreadsheets is how easy it is to make mistakes when creating, updating, and deleting data. Imagine entering names into a spreadsheet containing employee information. If you were careless, you might accidentally enter someone's name twice, or even write their date of birth instead. A spreadsheet doesn't prevent you from making these mistakes, but databases can! Databases are capable of validating the integrity of the data, resulting in much less redundant, missing, and incorrect information.

- png of excel sheet with dirty data

### Safe Concurrent Access
When multiple users are simultaneously accessing a database, the database ensures that each user's operations don't interfere with one another. On the other hand, spreadsheets give no guarantee of such safety. Imagine hundreds of users accidentally overwriting each others changes on a spreadsheet. The result could be potentially disastrous with cases of inconsistent or missing data. 

### Security
Databases make it much safer to deal with sensitive data. Users can be given different permissions that determine what kinds of database operations they're allowed to conduct. You don't necessarily want all users to have complete control over a database, and you definitely don't want to risk exposing private information to the public.

<br>

## ETC

A DBMS is a type of software that 


But let's think for a moment. Could something like an Excel spreadsheet be considered a database? Using a spreadsheet, you could certainly organize data in a tabular format where rows represent records and columns represent attributes. 

- png of excel spreadsheet

Seems pretty organized to me. Going by our original definition, you could definitely label a spreadsheet as a database. However, we are tech folk! When we talk and think about databases, we probably aren't visualizing Excel or Google Sheets. The databases we mull over do more than just hold organized data sets. They're efficient. They keep our data clean. They support an extra layer of features that spreadsheets don't have. So let's narrow down our definition to better fit our mental model.









A database is an organized collection of data. Although generally stored and accessed electronically from hardware, physical paper-based databases were definitely more common in the past, a good example being phonebooks.

## DBMS

Surprisingly, databases do not need to be stored and accessed from hardware to be classifised as one, although they generally are. Physical paper-based databases were definitely more common in the past (e.g. phonebooks), but did not provide the benefits.

 Although databases are generally stored and accessed electronically from hardware, they do not need to be. Physical paper-based databases were definitely more common in the past (e.g. phonebooks).

 Although virtually all databases today are computerized,



"A database is an organized collection of data, generally stored and accessed electronically from a computer system."

At its most basic form, a database is a **structured collection of data**. Surprisingly, databases do not need to be stored on hardware to be classifised as one. Although virtually all databases today are computerized, physical paper-based databases were the norm back in the day. What really defines a database is the fact that the data is stored in a **structured** manner. 




The tabular format is a popular database structure where data is organized into rows and columns

- what
- why
- dbms

However the databases of today are basically all computerized, so that will be our focus. 

interested in today are digital ones  are almost always referred to from a digital context! We will be focusing on computerized databases for the rest of the article. 

However since databases are almost always thought of as a digital entity,

 since databases are almost always being discussed and used from a digital context 

However, databases are almost always thought as   referred to from a digital context   It is natural that computerized databases are more relevant for us. So For the rest of the article we will be focusing on the benefits digital databases bring and the different types that exist.

So what does structured data actually look like? 

## Why are databases important?
- text on unstructured data


So what does structured data actually look like? Before that let's look at examples of unstructured data first.

 This means that the data should be organized in such a manner that will allow for efficient retrieval   

Unstructured data


 example, while an email may contain a large amount of data, it shouldn't be considered as a database since the data 

while email platforms can contain massive amounts of data, they should not be considered as databases since the data isn’t necessarily stored in a structured manner.

- png

On the other hand, physical phone books can be viewed as databases because household and phone number data are recorded in an alphabetical list format. 

- png

For the rest of this article we’ll be focusing on detailscomputerized databases - that is, a database stored in hardware. 



Although databases are typically stored on hardware, they don't have to be. What makes a database a database is whether the data is structured or not.

Alternatively, an Excel spreadsheet can be identified as a database if the data is organized in a tabular format.

Phonebooks are a good example of a physical paper-based database 

However, virtually all modern day databases are computerized so that'll be our focus 

 the databases of today are We will be focusing on computerized databases for the rest of the article. 

Given that the databases of today are essentially all computerized, we will be focusing on computerized databases for the rest of the article. 

This is because of the benefits they bring with efficient usage and  

Modern databases support efficient creation, retrieval, modification, and deletion of data. 

  it actually doesn't matter whether the data is stored digitally or physically (e.g. phonebooks), as long the data is structured it can be considered a database. However, virtually all databases in use today are computerized, so naturally we'll be diving into that. 

  Although it doesn't matter whether the data is stored digitally or physically to be considered a database, virtually all databases today are computerized. This is because of the benefits and efficiencies computerized databases provide.


  The storage mediums these companies use are called


  Consider all the organizations you've registered with in your lifetime. They probably range from non-essential services like Facebook and Club Penguin, to much more important ones such as banking and medical. Regardless of what you signed up for, it's a guarantee that your personal information has been stored somewhere. And it doesn't just stop with registrations. Sports teams keep track of player statistics, shops record daily transactions, literally every organization out there is interested in saving some kind of data. The storage mediums they use to accomplish this are called **databases**. 


On the other hand, manipulating data on a spreadsheet can be tedious work. Imagine being a business owner who uses a spreadsheet to track inventory. What happens if you want to delete all records

You have tens of thousands of records in your spreadsheet, a  You want to delete all   one at a time. You would have to manually search for each row 


### Easy and Efficient Operations
Databases make it very easy to create, find, sort, update, and delete data. All operations are optimized to be executed as quickly as possible.


provide many desirable features when dealing with large amounts of data.

Databases are more than just storage containers for data. If that's all they were capable of there would be little reason to choose a formal database over something like a spreadsheet. However, databases are designed to address important issues that come up when dealing with large amounts of data that more traditional storage mediums don't necessarily fix.


A database is an **organized collection of data that has rules upon that data**
So let's narrow down our definition to better fit our mental model.


Seems pretty organized to me. Going by our original definition, you could definitely label a spreadsheet as a database. However, we are tech folk! When we talk and think about databases, we probably aren't visualizing Excel or Google Sheets. The databases we mull over do more than just hold organized data sets. And that's because there's an extra piece here that isn't mentioned nearly as often as databases They're efficient. They keep our data clean. They support an extra layer of features that spreadsheets don't have. And this is because the databases we mull over aren't aren 

where rows represent records and columns represent record attributes. 