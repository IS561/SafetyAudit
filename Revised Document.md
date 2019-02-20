# Revised Document
## Feb, 19, 2019
## Group Members

* Abhilasha Salunke
* Aditya Kadrekar
* Brandon McFadden
* Linxi Liu
* Mohit Gupta
* Yanan Shen
* Yang Wu
# Entities:
**1. Room**

Definition:  An area where occupants live in, and it has walls, floor and ceiling. 

Attributes: 
* Room ID (positive discrete number): identify the room 
* Room Type (true value): either a workspace or a non-workspace/public area
* Capacity (positive discrete number): the maximum number of people a room can accomodate 



**2. Building**

Definition: A structure which has walls and a roof, in this case, it is a university building. 

Attributes: 
* Building ID (positive discrete number): identify a building  

**3. Room Exit Doors**

Definition: A door which occupants can get out of their room and get to the Corridors. 

Attributes: 
* Width
* Obstructed (true value)
* Fire-rate (true value): whether this room exit doors is fire-rated 
* Locked (true value)
* One-way (true value)

**4. Exit Doors within the building**

Description: The door between corridors and stairwell, through this door you can access the stairwell. The door must be fire-rated and closed all the time since it should separate the fire from other areas, such as corridors in the building. 

Attributes: 
* Width
* Locked (true value)
* Obstructed (true value)
* Fire-rated (true value): whether this exit doors is fire-rated 
* One-way (true value)

**5. Exit discharge doors**

Definition: Occupants can get away from the building to the staging area such as exit yard and exit court. 

Attributes: 
* Width
* Locked (true value)
* Obstructed (true value)
* Fire-rated (true value): whether this exit doors is fire-rated 
* One-way (true value)
  
**6. Aisle**

Definition: An aisle is a passage between rows of seats or items in a room. The aisle we mentioned here is the passage from the inside of rooms to the Room Exit Door. 

Attributes: 
* Width. It will be decided as follow: at least 28 inches if aisle is in a “Non-public Area”; at least 36 inches if it is in a  “Public Area” or a “no fixed seating area”; at least 44 inches if it is in a  “Two Sides of Seating”. 
* Obstructed (true value)

**7. Corridors**

Definition: A corridor is a passage in the building that has doors leading to rooms. 

Attribute: 
* Width
* Obstructed (true value)

**8. Stairwell**

Definition: A stairwell is the part of the building which leads the occupant to other floors of the building to move out of the building by directing it towards the Exit discharge doors , during a fire-hazard.

Attribute:  
* Separated (true value): if the stairwell is separated from rooms and corridors by fire-rated constructions. 
* Obstructed (true value): if the stairwell is obstructed

**9. Items/things**

Definition: The physical object which are big and heavy enough to generate the hindrance in the easy movement of occupants.

Attributes: 
* Size

**10. Door Sign**

Definition: Marks on the door to identify the function of the door. 

Attribute: 
* Visible (true value): if the door sign is visible to the occupants

**11. Occupants**

Description: A group of people who can access to or work in a building. 

Attribute: 
* Size (discrete number) : number of people who occupy the space

**12. Pathway**

Definition:A passage in front of doors that allows occupants to pass through the door and get to other areas. 

Attribute: 
* Width
 

**13. Staging Area**

Definition: an open and safe space serving as the destination of an evacuation. It can be a court or a yard. 

Attribute: 
* Capacity (discrete number): the number of people it can take

**14. Exterior exit balcony**

Definition: This is a balcony built outside the building. And people can escape outside in this way when a fire break out. 

Attribute: 
* Width
* Capacity (discrete number): the number of people it can take


# Relationships:
**1.Must Not Obstruct**

Items must not obstruct Room, Room Exit Doors, Exit Doors within the building, Exit discharge doors, Aisle, Corridors, Stairwell, Pathway

* Domain: Items
* Codomain: Room Exit Doors, Exit Doors within the building, Exit discharge doors, Aisle, Corridors, Stairwell, Pathway
* Cardinality : many to many (M : N) 
* Arity : 2

**2. Include**

Each door should Include a door sign

Room includes a room exit door


* Domain:Building, Room, Room Exit Door, Exit Doors within the building, Exit discharge doors
* Codomain: Room, Door Sign, Room Exit Door
* Cardinality : One to Many (1 : N) 
* Arity : 2


**3. Can Re-enter through**

Except for the Exit Doors within the building between Corridors and Stairwell, the occupants can re-enter through the other doors and that means the other doors are not one-way doors.

* Domain: Occupants 
* Codomain: Room Exit Door, Exit discharge doors 
* Cardinality: Many to Many (M : N)
* Arity : 2

**4. Separate**

Exit Doors within the building between Corridors and Stairwells should be the fire-rated door. Because in this way, Exit Doors within the building 
separate stairwells from other fire areas of corridors.  

Exterior exit balconies should separate staging area from rooms (Building Code of Utah, 2015 ).

Thus, stairwells and staging area can be present in a fire-rated construction area

* Domain: Exit Doors within the building, Exterior exit balconies
* Codomain: Stairwells, Corridors; Staging area, Room
* Cardinality : Many to Many (M : N)
* Arity: 3

**5. Should be maintained as wide as**

Pathway Width should be maintained as wide as Room Door Exit

Pathway Width should be maintained as wide as Exit Doors within the building between Corridors and Stairwell

Pathway Width should be maintained as wide as Exit discharge doors

* Domain: Pathway 
* Codomain: Room Exit Doors, Exit Doors within the building,  Exit discharge Doors
* Cardinality: One to One (1:1)
* Arity : 2



**6. Leads to**

Room Exit Doors lead to Corridors

Corridors lead to Exit Doors within the Building

Exit Doors within the Building lead to Stairwell

Stariwell leads to Exit discharge Doors 

Exit discharge Doors lead to Staging Area

* Domain: Room Exit Doors ,  Corridors, Exit Doors within the Building, Stairwells, Exit discharge doors
* Codomain: Corridors, Exit Doors within the Building,  Stairwells, Exit discharge doors,  Staging Areas 
* Cardinality: Many to Many (M : N)
* Arity: 2

# Group Rationale:

The second Group assignment consists of modification of the already constructed entities and relationships along with a schema and instance level illustration. The modifications of the entities and its relationship as per the comments of other group members was an interesting part to work on. After reading each group members comments it was quite fascinating to get other views about the group task provided. We had total six reviews from another group and one from the Professor. Each of the group member picked one review, evaluated it as per the case study and suggested their suggestions. The difficult task of collaborating each person’s suggestion and deciding which entity relationship we want to work on was quite crucial. We wanted to take each reviewer into consideration and decide whether there is a necessity to consider the review of that reviewer or not. We wanted to make sure that the comments mentioned by that reviewer is in relation with the case study and justifies the relationship with its entities. 

## Improvement’s for the Next Version:

## Evaluation of the Reviews:

As each of the group member had evaluated one review we decided to take into consideration the main points they mentioned and why we shall consider those suggestions and why we must not. We started with this approach as we wanted to make sure that each opinion is taken into consideration and we must not miss out any important point from the given reviews as it will directly be associated with the further tasks of the assignment.

**Reviews Considered:**

One of the reviewers mentions about Aisles and in the previous document he couldn’t find a proper entity relationship for aisle and didn’t understand that why aisle is so relevant in this case scenario. We appreciated the comment of this reviewer and gave a proper justification about this entity and a proper relationship, so it is self-explanatory, and any reader could find a relevance and understand it in a better way. The suggestion about Emergency exist mentioned by a reviewer was another point that drew our attention as in our earlier stage to we as a group had conflicting ideas about it and we went through this part again as per the suggestions and decided to work on this entity again. We decided to drop the dimensions of emergency exits as after careful consideration we were unable to find a proper justification to keep that entity in consideration. By doing this we were able to clear our understanding and misconception and come up with an appropriate Exit discharge door entity and the relationships associated with it. Some of our understanding about the entities chosen and its relationship was not quite up to the mark and their arity was inappropriate, as that highlighted that by a group member as well by the professor, we revised the entities chosen along with the relationships and justified it with proper explanation. For the arity, which means the quantity of entities in a relationship, it is truly that we made some mistakes in the previous document. 


**Reviews Not-considered:**

Considering University of Idaho as an entity was one of the suggestions given by a reviewer and we as a group didn’t quite consider this as an entity as we are classifying the ‘Safety Audits” entity relationships of a building we decided to not take this suggestion into consideration. One reviewer mentioned the confusion regarding the entity Room and Doors, we were also confused about whether we need to conclude as one entity “Room” and other doors in the building as attributes. If we do this way, it’s more difficult to figure out the difference between the doors and express the relationship with other entities. So, we define the doors with specific definition to clarify what the doors are, and they are essential entities from our perspective. It will be clear to draw the UML diagram with the relationship with other entities. 	

## Group Discussion:

We conducted a group meeting after the reviews from other group members were given. The reviews given by them were quite good and it enabled us to consider the basis of our assignment case study again. We started revising the entire document again and came up with solutions by making our understanding clear. The discussions lasted for hours and we were trying to get the insight of the case study in a more fruitful way.  We wanted to make sure that we were taking each review into consideration. After, a lot of discussion during our group meeting, we decided to pick up “Room”, “Building”, “Room Exit Doors”, “Exit Doors within the building”, “Exit discharge doors”, “Aisle”, “Corridors”, “Stairwell”, “Items”, “Door Sign”, “Occupants”, “Pathway”, “Staging Area”, “Exterior exit balcony” as our main 14 entities and classes, “Not Obstruct”, “Include”, “Re-enter”, “Separate”, “Should be maintained as wide as”, “Lead to” as our main 6 relationships. With these the most critical entities and relationships we can best describe the scenario “Safety audit”. In the former document, we presented 21 entities and 7 relationships. The relationships between the entities are not clear and we can find more relationships. So, we delete some entities and change the relationships. We delete the first three relationships and keep the relationship “include” and rewrite the scoping note. The relationship “requires” is paraphrased from “met the requirement of”, so we change the relationship into “be maintained as wide as”, which describes the width of doors or corridors should met the width requirement. We have changed the relationships and keep the relationship “includes”, and we rewrite some relationships including domain, codomain, arity and scoping document. 

The experience of conducting this analysis is intriguing and there are some controversial issues in our discussion. For instance, there are several kinds of doors in this scenario. Shall we express it with one entity “Doors” and display different attributes in detail? Or shall we express it with different entity names like “Room Exit Doors”, “Exit Doors within the Building”, and “Exit Discharge Doors” and make detailed description in the attributes? Can readers figure out what the specific entity represents without reading the attributes? Since we need to demonstrate them with UML diagram, it’s important to figure out the differences between the entities. The entity “Items”, do they really exist? The situation is that the items exist, but they should not be displayed on aisles, walkways and corridors to obstruct the way. The main experience as a group this time was understanding the entity and relationships of this case study in a proper manner. As we had an ample amount time as well as review from other groups and Professor, we were able to get few answers on the queries or approach that we had in mind. We literally had to brainstorm when we received the comments and we as a group were really happy about the final output that we had.

## <center>Reference</center>
Building Code of Utah.Section 1021 Egress Balconies. (2015). Retrieved from https://up.codes/s/egress-balconies.
