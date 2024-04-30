
# System Concept & Architecture

## Preface:
- the architecture of DBMS has evolved from early monolithic systems to modern DBMS packages.
	- Monolithic system is: one block integrated system.
	- modern DBMS is: modular in design with a client / server system architecture.
- the amount of data has growth enormously so a massive storage database with a lot of computers is now required to manage and store those data.
- the evolution let us replace the centralized main frame computer with the distributed workstation computer or personal computer with a network communication.




## Data models, Schemes & instances
#### Data abstraction:
- focus on hide the details of data organization and storage and focus on the essential features for improving the understanding of the data.
- different users can understand data at their preferred level.
#### Data model:
- concepts used to describe the database
#### Structure of database:
- data types, relations and constraints that applied to the data.
#### Basic operations:
- for describing the database (insert, update, modify, etc ..)
#### Dynamic aspects or behavior of DB Apps:
- allow The DB designer to specify a user-defined operation on the database.
- like Compute-GPA in, Student object.
#### Categories of data models:
- high level or conceptual data:
	- provide models close to users with low details.
- physical data model:
	- describe details of how data is stored on computer storage media.
	- for computer specialist not for end users.
- implementation data model:
	- provide a concept easy to understand by end users and still data is organized.
	- it is like something in the middle between physical and conceptual.
	- used in traditional commercial DBMS.
#### data base schemes:
- description of database specified during 
  DB design
- not change frequently.
- it is diagrams
- don't have all things about DB like relationships.
##### schema construct:
- each object in the schema such STUDENT, COURSES
##### DB states:
- current set or instances of DB.
##### Difference between schema & state:
- when defining new DB, we specify schema to the DBMS.
- now the DB state is empty state with no data.
- we get the initial state when the initial data is loaded
- from then, every time an update occurred we have a new state.
- and at any time the DB has current state.
- DBMS is responsible for ensuring that every state is valid for DB structure and constraint.
- stores description of data and schemes as a meta data. so the DBMS can refer to the data or the schema when ever it need.
- schema sometime called intention and the DB called extenion.


## Three-Schema Architecture and Data Independence:
#### The 3 Important Characteristic of DB approach:
- store, insulation & support.
- use catalog to store schema.
- insulation of program and data (make them independence).
- support multiple users view.
#### Three-Schema Architecture:
- internal, conceptual & external level.
- the main goal of 3-schema architecture is to separate the user application from the physical DB.
##### Internal level:
- has internal schema.
- describe the physical storage structure.
- describe the complete details and access paths.
##### Conceptual level:
- hide the detail of physical structure and focus on entities, data types & relationships with the constraints.
##### External level:
- Describe a part of the DB which the user is interest in and hide the rest.

#### Mapping:
- the 3 schema is only a description of data and the actual data is hidden in the physical layer.
- external schema for each user group.
- you must convert the request form the external to conceptual then to internal to do a process over database.
- for retrieval request, you must convert the extracted data from stored database to match the format of user's external view.

- **Mapping**: The process of converting requests between levels.


## Data independence:
- the ability to change in one schema at a level without having to change the schema in the next high-level.
#### Logical data independences:
- changing the conceptual schema without having to change the external schema.
#### Physical data independence:
- changing the internal schema without changing the conceptual schema, then the external schema.


## Data Languages:
- the interface of each categories of users.
#### Data definition language(DDL):
- specify the internal and conceptual schema and mapping between them.
#### Storage definition language(SDL):
- for the internal schema in the past...
- now, the file organization for operating system.
#### View definition language(VDL):
- specify mapping (Conversion of requests) between conceptual and external level.
- DDL is used to define both conceptual and external shcemes.




## DBMS interface:
#### Menu-based interface:
- a pull-down menu are popular in web-based interfaces.
#### Apps for Mobile devices:
- provide app to allow the user to access their data through mobile device.
#### forms-based interface:
- display a form for each user.
- user can fill all or part of the entries to insert new data.
- DBMS have forms specifications languages to help programmers.
- SQL forms:
	- form based language
	- using form design in conjunction with the relationship shcema.
- oracle forms:
	- component of the oracle products the provides features to design application forms.
#### Graphical user interface (GUI):
- display the schema to the user.
- the user can manipulating the schema using diagram
- used for menus and forms.