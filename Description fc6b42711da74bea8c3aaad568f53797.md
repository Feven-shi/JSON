# Description

### **What is GitHub page?**

GitHub Pages is ***a static site hosting service that takes HTML, CSS, and JavaScript files straight from a repository on GitHub and publishes as a website.***

There are three types of GitHub Pages sites: project, user, and organization. Project sites are connected to a specific project hosted on GitHub, such as a JavaScript library or a recipe collection. User and organization sites are connected to a specific account on GitHub.com.

To publish a user site, you must create a repository owned by your personal account that's named `<username>.github.io`. To publish an organization site, you must create a repository owned by an organization that's named `<organization>.github.io`. Unless you're using a custom domain, user and organization sites are available at `http(s)://<username>.github.io` or `http(s)://<organization>.github.io`.

The source files for a project site are stored in the same repository as their project. Unless you're using a custom domain, project sites are available at `http(s)://<username>.github.io/<repository>` or `http(s)://<organization>.github.io/<repository>`. 

### what is API?

**Application Programming Interface (API)** is a software interface that allows two applications to interact with each other without any user intervention. API is a collection of software functions and procedures. In simple terms, API means a software code that can be accessed or executed. API is defined as a code that helps two different software’s to communicate and exchange data with each other.

It offers products or services to communicate with other products and services without having to know how they’re implemented.

There are mainly four main types of APIs:

- **Open APIs:** These types of APIs are publicly available to use like OAuth APIs from Google. It has also not given any restriction to use them. So, they are also known as Public APIs.
- **Partner APIs:** Specific rights or licenses to access this type of API because they are not available to the public.
- **Internal APIs:** Internal or private. These APIs are developed by companies to use in their internal systems. It helps you to enhance the productivity of your teams.
- **Composite APIs:** This type of API combines different data and service APIs.

### what is the use of swagger?

Swagger (now known as the OpenAPI Initiative, under the structure of the Linux Foundation) is an open-source API testing framework for **describing your API by using a common language that is easy to read and understand by developers and testers, even if they have weak source code knowledge also** Swagger **allows you to describe the structure of your APIs so that machines can read them.**

# Project Description

### P**arking Website**

The objective of this project is to provide parking system and provide payment details based on parked time.

we used bootstrap, javascript, Html and css languages.

overlook :

The webpage has two columns, one on the right is for registering new car  and the left is for viewing and storing information about parked cars.

The information contains

- name of customers
- phone-number
- plate-number
- parked time (starting time)
- remove icon

How it works ?

first the user fill basic information and hit park button then the system will automatically add the user in the list on left column with the parked time and a remove icon.

once the user is ready to unpark he must click the remove icon, then the system will pop a message displaying the amount of time the car stayed and how much it costed the user. Here if the user want to remove the car at the same minute he/she won’t be required to pay. there is also an option to stay. 

### Movie-dashboard

The objective of this project is to fetch APIs and display different types of movies.

The home-page has 3 basic functionalities or services

The first one is search

- you can search for a movie using the search bar on the right-corner of the page and click on the binocular glasses then using the search term  `get_movies_by_search ()` method will fetch all movies related to the input term
- Here `get_movies_by_search ()` is called inside `add_searched_movie_to_dom ()` method which will add all fetched data and display it under the last title of the page ( similar content )
- inside `add_searched_movie_to_dom ()` there is also another function call `get_rate_by_id ()`  which will fetch rate of each movie using id
- once we got all the information we will write it inside `search_result`

The second functionality is displaying upcoming movies 

- There is a default movie picture with next icon. you need to click on the icon to display what movies are going to released soon.
- when the icon is clicked `get_movies ()` function is invoked. inside the function fetching is done and is written on two html elements, one for the image and the other for details of the movie.

The last function is automatically displaying tv-series and trending movies

- when the window load `tv()` is invoked and displays most popular tv shows
- it displays the rate, image, title and release date of each movie
- you can click on the image to view the trailer of the movie.
- when trending link is clicked, `pop()` method is called and similarly it fetches and display.

### Covid-Dashboard

This project provides you detail information about covid from all over the world.

Basically the project uses cards and maps.

how it works

- when the window loads `global()` method is invoked which is also called inside `update()` to pass country. since `update()` is only invoked in another function input for `global()` won’t be available, therefore it will display the global covid data.
- there is a list of country which you can use to view data about only this country. the pie chart and the table will be update accordingly
- `country()` method is used to create the select option of countries as HTML element from the API
- `update()` method is used to get the selected item( country) and send it to `global()` to get specific data
- then `global()` will send the data to `pie()` to change the appearance of the pie accordingly
- `ztable()` is used to create table data using API. this table will also update itself when its argument is not array, meaning when you select a country it’s data in JSON format is not array so it will distinguish what to display using  this.
- `firstmap`  is High-charts map which basically display cases of each country on map. the main point here is in the `foreach` loop, once we fetched our data from the covid API we want the map to display our data not from population API, so for each country using country code, if the code from our fetch matches the country code from the population API fetch then assign `p.value` to confirmed case.
- `pie()` accepts 5 variables confirmed, active, death, critical and recovered cases and displays them.
- `cases()` is an interesting map. the main idea is grouping countries inside the correct continent and display how many cases they got per day. so there is an array object `zseries`  which has property name of continents and we want to fetch each countries data from API and match its continent, once we got it’s continent we will store it inside that continent using `data` array object which consists of name of the country and the one case per day as value.
- The last map is `alldata` this map will provide 3D pie chart of what case you chose. there are buttons to choose from, when you click one of them the function will be invoked and have the value of the button as `this.value`  sent as an argument, then it stores the name and global data of selected case from all the continent as an array and displays it.
