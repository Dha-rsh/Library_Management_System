Library Management System
-------------------------

Title:    Book Shelf

Target Audience: Librarians

End Users: Students,College staff, Aspirant,Business,Comman Peoples, Book Worms, Narrator 

Type: Business to Business (B2B)   

Timeline: 2 weeks

Budget: nil

Total Members: 2


Features:
---------

   * User Registration & Login
   * User Profile-Admin, Librarian, Student, Narrator, Guest
   * Book Management -Add/Edit/Delete/View books
   * Search & Advanced Filters-By title, author, genre, ISBN, availability
   * Borrowing System - issue & return books with due dates
   * Availability Status -Real-time book status (Available/Issued)
   * Overdue Management-Auto fine calculation & reminders

Additional Features:
-------------------
* Notifications & Alerts-Due date reminders, new book arrivals
* Audiobook Upload & Streaming-Narrators can add and manage audio versions
* Review & Rating System -Users can review and rate books
* User Dashboard-View borrowed books, history, and profile
* Admin & Librarian Dashboard-User activity logs, system overview



class diagrams:
---------------
Class: UserRegistration

  {

- userID: int
- userName: String
- email: String
- password: String
- confirmPassword: String
- role: String  // "admin", "librarian", "student", "narrator", "guest"
  
  }

class: LoginPage

  {

  - userName: String
- password: String

  }     

class: UserProfile  

  {

- userID: int
- name: String
- email: String
- role: String
- address: String
- phoneNumber: String
- profilePicture: String

  }
  
Class: Book

  {

- bookID: int
- title: String
- author: String
- genre: String
- ISBN: String
- publishDate: Date
- description: String
- status: String  // "Available", "Issued"
- audioAvailable: boolean
- rating: float

  }

Class: BookManagement

  {

- book: Book
- addedBy: int  // userID of librarian/admin
- dateAdded: Date
- lastModified: Date

  }  

Class: SearchFilter

  {

- keyword: String
- title: String
- author: String
- genre: String
- ISBN: String
- availabilityStatus: String  // "Available", "Issued"
  
  }
  
Class Borrowing

  {

- borrowID: int
- userID: int
- bookID: int
- issueDate: Date
- dueDate: Date
- returnDate: Date
- isReturned: boolean
- fineAmount: float

  }
  
Class: AvailabilityStatus

  {

- bookID: int
- isAvailable: boolean
- currentHolderID: int  // userID of the person who borrowed
- expectedReturnDate: Date

  }
  
Class: OverdueManagement

  {

- borrowID: int
- userID: int
- daysOverdue: int
- finePerDay: float
- totalFine: float
  
  }

    



    
