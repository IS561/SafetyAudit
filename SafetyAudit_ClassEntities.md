# HW1 Group4 Safety Audit
## Feb, 4, 2019

### Group Members
*  Abhilasha Salunke
*  Aditya Kadrekar
*  Brandon McFadden
*  Linxi Liu
*  Mohit Gupta
*  Yanan Shen
*  Yang Wu

### Group Coordination
We did some initial discussions on Moodle. It was a little problematic to get everyone together as it (Moodle) is different from a messaging application. We made a Messenger group to tackle this problem. To ensure that everyone contributed significantly and we covered the task at a fast pace, we met at Grainger library. The idea behind this was work happens at a good rate when everybody is physically present and it's easier to share ideas rather than typing out ideas. Of course, Daniel was working with us remotely, so he did with work with us remotely and we were able to succesfully work with him. We used [Google Colab](https://colab.research.google.com/drive/1HlUCfTEGAGx_OOxKv-3FgAhTLkw7t11_) to write the inital markdown file collaborately. 

## Task Division among Group Members

**Entity Relationship** 
*   Corridors and yard – Linxi Liu
*   Emergency  exits – Mohit Gupta
*   Building Exits – Yang Wu
*   Aisle, Occupants and Room Exit – Yanan Shen

**Rationale/Discussion** 
*   Abhilasha Salunke
*   Aditya Kadrekar

**Document review**  
*   Brandon McFaden

## Obstructions Faced

*   Mode of Communication
*   Time Conflict

The mode of communication which we wanted to choose was slightly difficult and time consuming. On the forum we agreed to connect on Messenger, but it was difficult to find everyone on messenger due to each person’s privacy settings. We somehow managed to connect to each other but we almost lost 2 days for this, which lead to a delay for the task to be performed. Later, time conflict was a major concern that was hindering on starting our activity, that lacked us behind for getting collaborative questions during the TA hours. The challenging part was to coordinate with Brandon who is an online student. We wanted to ensure that his contribution was as significant as it was with us who met in person.

### Discussion
Since we are a diverse group, everyone had something interesting to contribute. The discussions started off with each of us having to read a portion of chapters 5 & 6 (Classes & Attributes) from Information Modelling for Archaeology and Anthropology. This was to get everyone on track with the problem statement. Further, the discussion became a little specific about exits and exit access requirements. The discussion was worth the time investment as we discovered some unique ways of approaching this problem statement.

At start it was quite difficult for us to understand about how to deal with the entities and the analyse their relationship. Everyone had their own oipinion as per their understanding. So after a lot of arguments and debate we decided to go by a stepwise approach. We started considering one entity at a time and decided to take each group members opinion on it. This approach helped us to clear our understanding in the right way. By this method we were able to deal with the entities and its relationship and later we had a clear picture about it.

Since the requirement was 20 entites and relationships in total, we had to look at the possible entities and relationships we could cover based on our problem statement. We studied some existing exit plans for big buildings and came up with the entities mentioned below. Building was like an umbrella term we cosidered since we are making an exit plan for the building foremost. The emergency exit and building exit were linked to Building since those 2 are the mandatory exits which any Building should have as a safety precaution especially the emergency exit. The building exit and emergency exit were further divided into different types of exits for the both since it's important to understand what kind of exits exist for the occupants. The reason for choosing Room Exit as an entity is quite straightforward. People stay in rooms in a building and it's important to have proper exits for such rooms such as well structured doorways, stairways, etc. We also thought of a Room which would be a place where we could assemble occupants in case of some dire emergency. Here, the capacity varied for various rooms. The Aisle areas for these rooms is also an important entity which we have considered since people will cross the Aisel to reach the room. 

Following were the entities and its relationship which we choose at the start to help us understand better :

Building: means a construction, it is the parent class of the entity Room. Building has a one to many association with Occupants, many to many association with Exit. 

Building ID: is a set of rules that specifies the standards for constructed objects like buildings. Building ID has a many to many association with Exit. 
Room: one of the separate sections or parts inside a building. Room has a one to many association with Aisle, a one to many association with Occupant, a one to many association with Walkway. Room is a subclass of Building.

Occupant: means the people that are in an area (Building or Room). There could be zero or more people in an area. Occupant has a many to one association with Room, a many to one association with Building, a many to many association with Exit. 

Aisle: an area between or along sections of seats in a theater, classroom, or the like. Aisle has a one to one association with Exit, a many to many association with Exit, a many to one association with Room.  

Walkway: any passage for walking. Walkway has a many to one association with Room, a many to many association with Exit. 

Pathway: a way that constitutes or serves as a path. Pathway has a one to one association with Doorway. 

Doorway: an entrance to a room or building through a door. Doorway has a one to one association with Pathway. 

Stairwell: an enclosure of stairwell. Stairwell Enclosure has a one to many association with Exit.   

Balconies: a open space outside a room or building. Balconies has a one to many association with Exit,building and room. 

Yard: an open space outside building. Yard has a one to one association with building ID.

Fire Door: a fire-resistant door to prevent the spread of fire. Fire Door has a many to many association with Emergency Exit. Fire Door is a subclass of Exit. 

Exit Door: a door that leads to outside. Exit Door has a many to many association with Emergency Exit. Exit Door is a subclass of Exit. 

Emergency Exit: a set of building and property regulations designed to establish a mandatory standard for a building's ability to resist the start and spread of a fire as well as facilitating the prompt and safe evacuation of the occupants. Fire Code has a many to many association with Exit, many to many association with Fire Door, many to many association with Exit Door.
 
Exit:  a place to go out or away. Exit is the parent class of Exit Door and Fire Door. Exit has many to many association with Building Code, many to many association with Fire Code, many to many association with Occupant, one to one association with Aisle, many to many association with Aisle, and many to many association with Walkway. 

### Solutions
Every group member came up with unique solutions for the Safety & Audit problem statement. The basic goal was to reach at a consensus by keeping everyone's suggestions into consideration and we managed to do that swiftly. We split up the Safety & Audity document (shared by the prof) into 6 parts and each individual had to come up with some entity classes and relationships for the parts assigned to him/her. We decided on more than 20 entities namely Building, Room, Room Exit, Building Exit, Aisle, Occupants, Room Door, Doorways, Balconies, Ramp, Stairways, Stairwell, Fire Door, Yards, Passages, Courts, Corridor, Gates.  Once everyone was ready with their solution for the parts assigned to them, we merged everything together and came up up with an entity-relationship (E-R) diagram as uploaded on the Messenger group.

## Final Decision

After our group discussion we decided to keep our group meetings before the TA hours, which will help our queries to be solved at the earlier stage. This will help us to continue our group discussion in the right direction and open more ideas and approach of every person in the group. Our time span for working on the group task will also increase by this method. Collaborating effectively with Brandon through video call is the next step that we are going to do, that will help us understand his point of view for the assignment in a clear way.

## Experience of the Group

It started from a quiet group at the start but as we started discussing about the assignment everyone had a unique approach for the question. Everyone’s approach helped in increasing other persons understanding and knowledge. Team collaboration and ownership is the point that every member really appreciated.

## Rationales

* Since our scenario is to analyze exit and exit access for building safety consideration, we considered the place we need to exit. ‘Room’ could be the first entity that we pointed out because room includes both ‘Occupants’ and ‘Aisles’. And ‘Room Exit’ is a class, which includes several methods for ‘Occupants’ to go out of the room. Such as ‘Room Door’, ‘Stairways’, and ‘Balconies’. The exits in the building can be distinguished from building doors and emergency doors. Their functions are different because emergency exits should be used in case of fire while the building exits are normally used as exits. Firedoors should be regarded as a fire-protection system and it is the subclass of entity 'Emergency Exit'. The stairwell is the way that people use when a fire happens and it's the subclass of entity 'Emergency Exit'. The building, room and balcony could accommodate occupants. And ‘Room Exit’ includes several sub-classes. Corridors are one of the most important part of a building, especially a building for school or office. Since corridors can hold lots of people, it helps people to get out of the building during emergencies. Therefore, corridors is necessary to consider. Yard can be understand as the destination of an emergency evacuation and therefore we need to consider it. 


#  Entities

## Emergency Exit:

* Emergency exit serves as a way to move out of a particular section of a building or non-building structure like an event venue.

### Exergency exit attributes:

* Exit ID 1..\* (Number)
* Section Location Type: 1../* (Number)
* Total number of exits 1../* (Number)
* Type 1..2 (Text)

## Emergency exit doors:

* This represents the type of the entries that are present at the exit. 

* The doors can have bars on them that can be pushed to open the doors or the doors can have key locks on them.

* Remarks: There can be more than one type of emergency doors like a door with bars or a door without a lock, et cetera.


### Emergency exit door's attributes:

* Locked (Boolean)
* Present (Boolean)
* Weight (Number)
* Push Type Doors (Boolean)


## Connecting Section:

* It is an important entity which describes that which section of the building or the non-building venue gets connected from the emergency exits.

* Example: A movie theatre also has emergency exits, but that does not always directly leads to the exit door from the whole building directly. It sometimes exits to the sections that lead to the part towards the building exits.

### Connecting section's attributes:

* Building Exit (Boolean)
* Section entrance (Boolean)

## Ease of Accessibility:

* The buildings in the United States gives great importance on the ease of movement for the disabled individuals in the building. Various options like motorised doors are available for them.

* Presence of ramp in the building also counts under ease of accessibility as the disabled individual would find it difficult to climb the stairs.

* Example: Illini Union at the University of Illinois, Urbana Champaign has different doors on all the four entrances of the building for disabled individuals which do not requires any other human's assistance to open the doors for them.

* Remarks: Not all the buildings in the world are designed with such great details keeping in mind about the comfort of the person who accesses the building.

### Ease of Accessibility attributes:

* Automatic doors (Boolean)
* Doors Present (Boolean)
* Ramp (Boolean)


## Dimensions of Emergency Exit:

* Dimensions of emergency exit are essential as it can be a deciding factor for the number of people who can use it to move out of a section. Bigger the size of the exit, faster and easier it would be to clear the people from the part and move in or out great big machines or other items in or out of the section.

* Example: I saw a movie where a hospital caught fire, and the hospital staff found it difficult to move the patients on speciality machines out of the emergency exits because of the smaller dimensions of the emergency exit.

### Dimension attributes:

* Width 1../* (Number)
* Height 1../* (Number)


## Room

*   Room is a part of a building that has its own walls, floor and ceiling. It is a subclass of Building. 

### Room attributes：

*   Room ID (number)
*   Capacity (quantity)

## Aisle

*   Aisle is a passage between rows of seats within rooms.

### Aisle attributes:

*   Aisle ID (number)
*   Room ID (number)
*   Width (quantity)

## Room Exit

*  Room Exit is a method for occupants to go out or away from room. Examples include: go out of a room through “room door”, “stairways”, and “balconies”

### Room Exit attributes:

*   Room Exit ID (number)
*   Exit Access (boolean)
*   Exit Type (text)

## Room door

*   Room door is a way out of the room. 

### Room door attributes:

*   Room ID (number)
*   isBlocked (boolean)

## Door way

*   Door way is an opening in to a building or room.

### Door way attributes:

*   Door ID (number)
*   isBlocked (boolean)

## Balconies

*   Balconies are platforms on the outside of a building, above ground level, with a wall or railing around it. 

### Balconies attributes:

*   Balconies ID (number)
*   isBlocked (boolean)

## Ramp

*  It is a slope joins two parts of a road or path, which can assist occupants get out of the building quickly. 

### Ramp attributes:

*   Ramp ID (number)
*   isBlocked (boolean)

## Stairway

*   It is a set of stairs inside or outside of the building. 

### Stairway attributes:

*   Stairway ID (number)
*   isBlocked (boolean)

## Occupants

*   Occupants are people who live or work in a particular room or building. 

### Occupant attributes:

*   Occupants ID (number)
*   Number (quantity)


## Building

* A Building means a construction, which is a structure with a roof and walls standing in one place. It's the parent class of the entity Room, Building Exit, and Emergency Exit. 

### Building attributes

* Building ID (number)
* Building Name (text)

## Building Exits

* A Building Exit means a door which connects the inside with the outside of the building. It's the subclass of the entity Building. 

### Attributes of Building Exits

* Building Exit ID (number)
* Building Exit Type (text)

## Emergency Exits

* An Emergency Exit is a special exit for emergencies such as a fire. It's the subclass of the entity Building. 

### Emergency Exits Attributes 

* Emergency Exit ID (number)
* Emergency Exit Type (text)

## Fire Doors

* A Fire Door is a door with a fire-resistance rating used as part of a passive fire protection system. It's the subclass of the entity Emergency Exit. 

### Fire Doors Attributes 

* Fire Door ID (number)
* isLocked (boolean)

## Stairwells

* A Stairwell is a construction designed to bridge a large vertical distance by dividing it into smaller vertical distances. It's the subclass of the entity Emergency Exit. 

### Stairwells Attributes

* Stairwell ID (number)
* isLocked (boolean)


 
## Corridors

* A corridor is a passage within the building that has doors lead into rooms. It also connects to fire doors and stairwell for emergencies. Corridors can accomodate large group of occupants for fast egress.

### Corridor attributes

* Corridor ID (number)
* Width (number)
* isBlocked (boolean)

## Yard

* A yard is an area that immediately adjacent to a building or a group of buildings. It is an open space and can accomodate large group of occupants. It is connected to buildings with stairwells, building exits, and/or emergency exits.

### Yard attributes

* Yard ID (number)
* Area (number)


# Relationships

## Accessible by:

* Scope note: An emergency exit can be accessed and used by a disabled individual.
* Domain: Exit
* Codomain: Automatic doors, Ramp, Light Weight Doors
* Arity: 2
* Cardinality: 1..\*


## Towards:

* Scope note: Emergency exit leads toward room exit, inner section exit or building exit.
* Domain: Exit
* Codomain: Building section, building exit, stairways, ramp
* Arity: 2
* Cardinality: 1..\*


## Used by:

* Scope note: It can be used by disabled individuals apart from healthy individuals.
* Domain: Exit
* Codomain: Handicapped and non-handicapped individual
* Arity: 2
* Cardinality: 1..2

## Accommodate

*   Scope note:Providing lodging or sufficient space, it can be any physical space, especially a building. For example, a Room can accommodate zero or more Occupant.
*   Domain: Room, building, corridors, yard, balcony
*   Codomain: Occupant
*   Arity: 6
*   Cardinality: one-to-many


## Includes

*   Scope note: Comprise or contain as part of a whole.
*   Domain: Room Exit, Room
*   Codomain: Room Door, Doorway, Balconies, Ramp and Stairways, Aisle
*   Arity: 8
*   Cardinality: Associate (sub-class)
*   Remarks: There are several ways that occupants can get out of the room. ‘Room Exit’ has several types of exiting methods. 


## Requires

*   Scope note: Participation of width of aisles, walkways and corridors
*   Domain: Occupancy
*   Codomain: Width
*   Arity: 2
*   Cardinality: one-to-many
*   Remarks: Consider the room occupancy(50 is the boundary) and then decide the requirements of width of aisles or walkways. 

## Allow immediate access

*   Scope note: Aisles, walkways and corridors must be clear enough to allow immediate access to exits
*   Domain: Aisles, walkways, corridors
*   Codomain: Exits
*   Arity: 2
*   Cardinality: many-to-many
