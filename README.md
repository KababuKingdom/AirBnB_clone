# AirBnB_clone

![image](https://user-images.githubusercontent.com/27401241/123797101-816aac80-d8ee-11eb-8aac-13362397f7fa.png)


The AirBnB clone project is a simple copy of the [AirBnB website](https://alx-intranet.hbtn.io/rltoken/m8g02HcD2ovrl_K-zulYBw) that will be deployed on a server.

It implements only some of the features that cover fundamental concepts of the higher level programming track.

## Components

This project will be built step by step not all at once. It has different components.

## The Console

This software is a command interpreter similar to a Linux shell but limited to a specific use-case; management of objects in the AirBnB Clone:

-   Creating new objects (ex: a new User or a new Place)
-   Retrieving an object from a file, a database etc…
-   Doing operations on objects (count, compute stats, etc…)
-   Updating attributes of an object
-   Destroying an object

The first piece is to manipulate a powerful storage system. The storage engine gives an abstraction between the objects and how they are stored an persisted. It will allow easy change in storage without need to update the entire codebase.

![image](https://user-images.githubusercontent.com/27401241/123797176-96dfd680-d8ee-11eb-9414-ee496ec466e3.png)

## How to start it
These instructions will get you a copy of the project up and running on your local machine (Linux distro) for development and testing purposes.

## Installing

You will need to clone the repository of the project from Github. This will contain the simple shell program and all of its dependencies.


git clone https://github.com/kababukingdom/AirBnB_clone.git
```
After cloning the repository you will have a folder called AirBnB_clone. In here there will be several files that allow the program to work.

> /console.py : The main executable of the project, the command interpreter.
>
> models/engine/file_storage.py: Class that serializes instances to a JSON file and deserializes JSON file to instances
> 
> models/__ init __.py:  A unique `FileStorage` instance for the application
> 
> models/base_model.py: Class that defines all common attributes/methods for other classes.
> 
> models/user.py: User class that inherits from BaseModel
> 
>models/state.py: State class that inherits from BaseModel
>
>models/city.py: City class that inherits from BaseModel
>
>models/amenity.py: Amenity class that inherits from BaseModel
>
>models/place.py: Place class that inherits from BaseModel
>
>models/review.py: Review class that inherits from BaseModel

#### Usage

The console can be used both interactively and non-interactively.


#### *Interactive Mode*
```
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) 
(hbnb) 
(hbnb) quit
$

```

 
#### *Non-Interactive Mode*
```
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 

#### The commands

*Command*       |  *Function*                                 |  *Usage* 
----------------|---------------------------------------------|-----------
**quit or EOF** | Exits the program | By itself 
**help**        | Provides a text describing how to use a command.  |  By itself --or-- **help <command\>**
**create**      | Creates a new instance of a valid `Class`, saves it (to the JSON file) and prints the `id`.  Valid classes are: BaseModel, User, State, City, Amenity, Place, Review. | **create <class name\>** 
**show**        | Prints the string representation of an instance based on the class name and `id`  |  **show <class name\> <id\>** --or-- **<class name\>.show(<id\>)**
**destroy**     | Deletes an instance based on the class name and `id` (saves the change into a JSON file).  | **destroy <class name\> <id\>** --or-- **<class name>.destroy(<id>)**
**all**         | Prints all string representation of all instances based or not on the class name.  | By itself or **all <class name\>** --or-- **<class name\>.all()**
**update**      | Updates an instance based on the class name and `id` by adding or updating attribute (saves the changes into a JSON file).  | *update <class name\> <id\> <attribute name\> "<attribute value\>"** ---or--- **<class name\>.update(<id\>, <attribute name\>, <attribute value\>)** --or\-- **<class name\>.update(<id\>, <dictionary representation\>)**
**count**       | Retrieve the number of instances of a class.  | **<class name\>.count()**

## Authors

<p>Solomon Kababu - kababukingdom@gmail.com</p>
