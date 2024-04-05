# Project Standarts

## What sould endpoints look like?

### Front-end

A **front-end endpoint** (or client url) start should look like this: ``https://tales.forgepen.com/`` and then continue depending on the module required

- **Root**

  ``/``: Homepage - Dashboard

- **Auth**

  ``/login``: login page

  ``/signup``: signup pagess

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

  ``/search``





### Back-end

A **back-end endpoint** (or API url) start should look like this: ``https://talesapi.forgepen.com/`` and then continue depending on the module 

> **ATENTION:** Backend API can **ONLY** return an *image* or a *JSON object*