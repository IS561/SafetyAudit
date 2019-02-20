# Revised Document
## Feb 19, 2019
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



## <center>Reference</center>
Building Code of Utah.Section 1021 Egress Balconies. (2015). Retrieved from https://up.codes/s/egress-balconies.
