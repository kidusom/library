Core Features  

CRUD Operations:
Books:  create, read, update, and delete books.
Users:  user registration and management.
Transactions: users can borrow and return books. 

1.Create user
    Post  >>  https://kidusom.pythonanywhere.com/api/users/
    Content type >> application/json
    Body >> 
    {
     "username": "user4",
     "password": "user4password",
     "email": "user4@user4.com",
     "first_name": "user",
     "last_name": "4"
    }


2.Get user auth token 
          Post  >>  https://kidusom.pythonanywhere.com/api/token/
         Content type >> application/json
       {
        "username": "user4",
        "password": "user4password"
       }

3.Delete user
    Delete >> https://kidusom.pythonanywhere.com/api/users/5/
    Token >> Authorization,bearer
    Content type >> application/json



4.List users
     Get >> https://kidusom.pythonanywhere.com/api/users/
     Content type >> application/json


5.Create book
    Post >> https://kidusom.pythonanywhere.com/api/books/
    Content type >> application/json
    Body >>
    {
     "title": "Across the Sand",
     "author": "hugh howey",
     "isbn": "9780061120085",
     "published_date": "2022-10-04",
     "copies_available": 30
     }


6.Delete book
    Delete >> https://kidusom.pythonanywhere.com/api/books/4/
    Content type >> application/json


7.List books
      Get >> https://kidusom.pythonanywhere.com/api/books/
      Content type >> application/json


8.Borrow book
      Post >> https://kidusom.pythonanywhere.com/api/transactions/check_out/
      User2  >> Authorization,bearer
           Content type >> application/json
           Body  >> 
           {
           "book_id": 1
           }


9.Return book
     Post >> https://kidusom.pythonanywhere.com/api/transactions/return/
          User2  >> Authorization,bearer
           Content type >> application/json
           Body  >> 
           {
           "book_id": 1
           }


10.See copies 
     Get >> https://kidusom.pythonanywhere.com/api/transactions/history/
          User2  >> Authorization,bearer
          Content type >> application/json


11.See transaction history 
     Get >> https://kidusom.pythonanywhere.com/api/books/1/
         Content type >> application/json   


12.Errors 
        Checkout book twice 
       And return book i didn't not borrow 
           Post >> https://kidusom.pythonanywhere.com/api/transactions/check_out/
       User2  >> Authorization,bearer
           Content type >> application/json
           Body  >> 
           {
           "book_id": 1
           }
 
