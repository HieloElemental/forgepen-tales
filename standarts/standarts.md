# Project Standards

## What should endpoints look like?

> **Note:** A parameter on the url that ends with the word ``...List`` must be an **array** separated with commas ``,``

### Front-end

A **front-end endpoint** (or client url) start should look like this: ``https://tales.forgepen.ink/`` and then continue depending on the module required

- **Root**

  ``/``: Homepage - Dashboard

- **Auth**

  ``/login``: login page

  ``/signup``: signup pages

- **Profiles**

  ``/users``: see list of popular users

  ``/user/${userID}``: see an user info

  ``/user/edit``: edit logged user info

- **Books**

  - **Explore/View**
  
    ``/books``: see the explore view

    ``/read/${userName}/books``: see an author books

    ``/read/${userName}/${bookSharingID}``: see the book information menu

    ``/read/${userName}/${bookSharingID}/chapters``: see the book chapters menu

    ``/read/%{userName}/${bookSharingID}/${chapterNumber}``: see a chapter elements

  - **Manage/Edit**

    ``/write/${userName}/${bookSharingID}``: edit the book information

    ``/write/${userName}/${bookSharingID}/chapters``: edit the chapters of a book (add/view/rename/delete)

    ``/write/${userName}/${bookSharingID}/${chapterNumber}``: edit the chapter info

- **Search**

  ``/search/global/${searchQuery}``: made for general search

  ``/search/book/${tagsList}/${searchQuery}``: search a book with some tags included

  ``/search/user/${tagsList}/${searchQuery}``: search a user with some tags included

- **404**

  ``/404``: not found error page


### Back-end

A **back-end endpoint** (or API url) start should look like this: ``https://talesapi.forgepen.ink/`` and then continue depending on the module 

> **ATTENTION:** Backend API can **ONLY** return an *image* or a *JSON object*

- **Auth**

  ``(POST)/auth/login``: Get the username and password from the client and make the authentication logic

  ``(POST)/auth/verify-token``: Verify the token given by GoogleOAuth API to authenticate the user via Google

  ``(POST)/auth/signup``: Sign up the user with given data

- **Profiles**

  ``(GET)/user``: Get the registered user information

  ``(GET)/user/${userName}``: get an specific user information, books and popular contributions.