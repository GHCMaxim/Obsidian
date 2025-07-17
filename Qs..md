
### Scenario

You are tasked to create a simple library management system for your local library. The system should start with these 4 simple classes: `Book`, `Member`, `Librarian`, `BorrowTransactions`.

For the sake of not wasting too much time, here's a sample design setup. You **MAY** change the design as necessary:
![[Untitled(10).png]]

### Question 1: (OOP)
a. How would you use Object-Oriented principles like *inheritance* or *polymorphism* to model the system?
- Create a `Librarian` class that directly inherits from `Member`. (inheritance)
- Both `Member` and `Librarian` can `viewBooks()`, however `Librarian` would overrides the method to allow for book management. (this counts as polymorphism.)
b. How would you ensure that each Member borrowing books would be protected using *encapsulation*?
- By keeping `isAvailable` private in `Book` class and exposing a `borrow()` method to check and updates if a book is available.
- Keeping `borrowedBooks[]` private in `Member`, with controlled methods.
c. How can you ensure that a Librarian can have additional permissions, like adding books, or removing books?
- By extending the `Member` class, and adding new methods like `addBook()` or `removeBook()`
- Both `Member` and `Librarian` can `viewBooks()`, however `Librarian` would overrides the method to allow for book management. (ironically also a correct answer.)
### Question 2: (DSA)
Suppose your system needs to keep track of borrowing book efficiently:
a. What *data structure* would you use to store books, for a fast lookup (Hint: ISBNs are unique and is a list of numbers.)
- Consider storing `Book` records in `HashMap<ISBN, Book>` to abuse it `O(1)` lookup.
- Alternatively, you can just use `int` and throw all ISBN searches into a Binary Search Algorithm and work from there.
b. In case there's multiple wanting the same book, but it is already borrowed, how would you keep track of who to give the book to first, after it's available again?
c. (Bonus Question) Supposedly you need to create a recommendation system for your members, what *data structure* would you use as a base to implement?
- You throw it into a Decision Tree of some sort, likely a balanced Binary Tree

### Question 3: (SQL):
a. Write a query to get the list of books borrowed by a member with `MemberID = 1001`.
b. How would you join the `Book` and `BorrowTransaction` tables to find books currently borrowed and by whom?
c. How would you create an index to optimize searching for a book by `ISBN`?
d. How would you select all overdue borrowings?
### Question 4: (SDLC)
a. Which SDLC model would you use, Agile or Waterfall. Explain the difference between these models, and why is one possibly preferred over the other.
b. Where would **CI/CD** fit into this project workflow, on the SDLC model you chose?

### Question 5: (Bonus)
a. If you need to handle thousands of transactions per second, what changes might you consider in your *database design* (Indexing, Normalization, Denormalization)?
b. If you do consider caching, where would you consider placing it? At the database level, at the programming level, etc..
c. Would your OOP design support scalability and maintainability over time?


