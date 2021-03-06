# Obux
##### [Clique aqui para a versão em português](./readmeStuff/readmeBR.md)


<p align="center" style="display: flex; align-items: center; justify-content: space-around">
  <img src="./readmeStuff/LOGO.png" alt="obuxLogo" width="250">
</p>
<p align="center">Obux is an app that helps you borrow and trade books with other people.</p>
<br/>

Obux Will let you trade books with someone that has a book of your interest, borrow someone's else book or put your own books up for trades and for other people to borrow.
<br/>

## Technologies Used
<p align="center" style="display: flex; align-items: center; justify-content: space-around">
  <img src="./readmeStuff/nodejs_logo.png" width="100">
  <img src="./readmeStuff/mongo_logo.png" width="100">
  <img src="./readmeStuff/rn_logo.png" width="100">
</p>

For this project, we've used NodeJS for the Backend, MongoDB for database and ReactNative for the Frontend (without Expo).
<br/>

## Documentation Summary
* ### [How to run](#how-to-run-it)
* ### [Routes](#project-routes)
* ### [Models](#project-models)

## How to run it
#### BackEnd
First you got to setup the BackEnd. For this, download [NodeJS](https://nodejs.org/en/)
<br/>
After it, you must download the dependencies by executing the following commands

```console
hello@world:~$ yarn
```

And now, all you gotta you do is run. Just run this command (Don't forget to set the environment variables in a .env file)

```console
hello@world:~$ node app.js
```

#### FrontEnd
First, you've gotta download and install React Native (without expo) and just run the following command in the frontend folder

```console
hello@world:~$ react-native run-android
```

# Project Routes

### User Routes
|       Route           |    Method    |                   Description                    |                                                                         
|   :---------------:   | :----------: | :----------------------------------------------: |                                                                           
|  `/createuser`        |    POST      |  Route that creates a User                       |                                                         
|  `/getuser/:id`       |    GET       |  Gets the user by its ID                         |   
|  `/login`             |    POST      |  Route for user login                            |                                                        
|  `/deluser/:id`       |    DELETE    |  Deletes the user by its ID                      |                 
|  `/updateuser/:id`    |    PUT       |  Updates the user by its ID                      |                                                     
|  `/rateuser`          |    POST      |  Creates a rating for the user based on reviews  |
|  `/finduser`          |    POST      |  Find a user by its city and/or state            | 

### Book Routes
|       Route       |    Method    |                                 Description                                  |                                                                                                          
| :--------------:  | :----------: | :--------------------------------------------------------------------------: |                                                                           
|  `/registerbook`  |    POST      |   Route that creates a book                                                  |                                                         
|  `/getbook/:id`   |    GET       |   Gets book by its ID                                                        |   
|  `/delbook:id`    |    DELETE    |   Delete book by its ID                                                      |                                                        
|  `/updatebook:id` |    PUT       |   Updates a book by its ID                                                   |                 
|  `/findbook`      |    POST      |   Route to search for books by its name, genre, year or author               |

### Pass Recovery Routes
|       Route            |    Method    |                                 Description                                  |                                                                                                          
| :--------------:       | :----------: | :--------------------------------------------------------------------------: |                                                                           
|  `/request`            |    POST      |   Route that sends the pass recovery email                                                  |                                                         
|  `/recovery/:token`   |    GET       |   Checks token                                                       |   
|  `/redefinepassword/:token`         |    POST    |   Redefine password                                                      |                                                        

# Project Models

### User Schema
| FieldName  | Translated    | Type                                   | Required | Unique |
|:------------:|:---------------:|:----------------------------------------:|:---------:|:--------:|
| `nome`       | name          | String                                 | true    | false  |
| `dataNasc`   | birthday      | Date                                   | true    | false  |
| `telefone`  | mobile number | String                                 | false   | true   |
| `email`      | email         | String                                 | true    | true   |
| `cpf`        | cpf           | String                                 | true    | true   |
| `senha`      | password      | String                                 | true    | false  |
| `cidade`     | city          | String                                 | true    | false  |
| `estado`     | state         | String                                 | true    | false  |
| `biblioteca` | library       |  \[mongoose\.Schema\.Types\.ObjectId\] | false   | false  |
| `pfp`        | profile pic   | String                                 | false   | false  |
| `givenrates` | givenrates    | Number                                 | false   | false  |
| `totalrates` | totalrates    | Number                                 | false   | false  |


### Book Schema
| FieldName       | Translated   | Type   | Required |
|:-----------------:|:--------------:|:--------:|:---------:|
| `titulo`          | title        | String | true    |
| `autor`           | author       | String | false   |
| `ano`             | year         | String | false   |
| `genero`          | genre        | String | false   |
| `qualidade`       | quality      | Number | true    |
| `foto`            | Photo        | String | false   |
| `disponibilidade` | availability | Number | true    |
| `sinopse`         | synopsis     | String | false   |

## Design
[Click here to check the app design at figma](https://www.figma.com/file/tAH0UaEkDmD9pgSNjInOwj/Untitled?node-id=157%3A177)

## Project Members
| <img src="https://avatars.githubusercontent.com/jonatasfernandespimenta" width=115> | <img src="https://avatars.githubusercontent.com/LucaKmit" width=115> | <img src="https://avatars.githubusercontent.com/murilindo" width=115> | <img src="https://avatars.githubusercontent.com/JulioCelloto" width=115> | <img src="https://avatars.githubusercontent.com/capjackOrigins" width=115> |  
|---|---|---|---|---|
| <a href="https://github.com/jonatasfernandespimenta">Jônatas</a> | <a href="https://github.com/LucaKmit">Luca</a> | <a href="https://github.com/murilindo">Murilo</a> | <a href="https://github.com/JulioCelloto">Julio</a> | <a href="https://github.com/capjackOrigins">Pedro</a> |
