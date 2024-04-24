# Database Tables

Using a SQL relational base database we have the next tables (there can be future changes):

> **Note:** only direct database interactions are allowed to use the underscore character (_) in column names, 

## Users table

### Basic

| Name | Description | Key |
|------|-------------|-----|
| user_id | Auto generated Id for a user, inalterable, unique and should not be shown to the client | Primary |
| user_name | Alterable but UNIQUE name for the client-side connections of a user |
| user_display_name | Also alterable but not-unique name that is shown for a user |
| user_description | User description |
| user_created_at | Date when the user was created |
| user_last_contribution | Last time when the user interacted with a book |
| user_is_verified | A user that has been verified by an admin |

### Google Information

| Name | Description | Key |
|------|-------------|-----|
| google_sub | User's unique Google ID |
| user_email | User's google email |
| user_email_verified | Shows if the google email is verified |

> **Note:** If a user is verified it will have a verified symbol to indicate it so.

## Book-info table

| Name | Description | Key |
|------|-------------|-----|
| book_id | Auto generated Id for a book, unique and should not be shown to the client | Primary |
| book_name | Alterable but UNIQUE name for the client-side connections of a book |
| book_display_name | Also alterable but non-unique |
| book_description | Book description |
| book_synapse | Book trama description |
| book_chapters_name | How chapter names would be like |
| book_chapters_number_type | How will the chapters numbers will be displayed |
| book_created_at | Date when the book was created |
| book_last_contribution | Last contribution date |
| book_user_id | Link to the user creator of the book | Foreign |


## Book-chapters table

| Name | Description | Key |
|------|-------------|-----|
| chapter_id | Auto generated Id for a book, unique and should not be shown to the client | Primary |
| chapter_name | If the chapter has a name |
| chapter_number | Organize a book's chapters order an what number would be displayed in the chapter |
| chapter_genre_list | Array of the different genres of the book |
| chapter_created_at | Time when the chapter was created |
| chapter_last_contribution | Last chapter contribution date |
| chapter_book_id | Connection to the book from the chapter | Foreign |
| chapter_user_id | Connection to the contributor user | Foreigsn |

