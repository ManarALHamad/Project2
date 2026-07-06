# Project2


| HTTP Method (Verb) | Path/Endpoint/URI     | CRUD Operation            | Route Name | Has Data Payload? | Purpose                                                                                            | Render/Redirect Action        |
| ------------------ | --------------------- | ------------------------- | ---------- | ----------------- | -------------------------------------------------------------------------------------------------- | ----------------------------- |
| GET                | `/books`              | Read all _books Names_          | index      | No                | Renders a view that shows all books Names and categories                                                              | `res.render('books/index')`   |
| GET                | `/books/:bookId`      | Read a specific _book_    | show       | No                | Renders a view that shows a specific book                                                          | `res.render('books/show')`    |
| GET                | `/books/new`          | None                      | new        | No                | Renders a view including a form that the user can fill to suggest a new book (title, category)                | `res.render('books/new')`     |
| GET                | `/books/:booksId/edit` | See note below*           | edit       | No                | Renders a view including a filled out form to edit the book language | `res.render('books/edit')`    |
| POST               | `/books`              | Create a new _book_       | create     | Yes               | Handles the user submitting a form to create a new book                                           | `res.redirect('/you-choose')` |
| PUT                | `/bookss/:book`      | Update a user's _book_  | update     | Yes               | Handles the user submitting a form to update their book                                       | `res.redirect('/you-choose')` |
| DELETE             | `/bookss/:bookId`      | Delete a specific _book_  | delete     | No                | Handles the user request to delete a specific book from their currently reading books                                                  | `res.redirect('/you-choose')` |

*NOTE: The `edit` route may optionally read data for a specific books editing.
