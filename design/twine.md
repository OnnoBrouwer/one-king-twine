# Twine passages

Passage      | Description
-------------|------------
StoryInit    | Initialize variables
StoryMenu    | Load sidebar with present / regard and undo actions if Conan active; add Credits and Achievements
Credits      | Show credits and navigate back to Prologue / Epilogue / Room passage
Achievements | Show achievements (if any) and navigate back to Prologue / Epilogue / Room passage
Prologue     | Show prologue and navigate to Room passage
Epilogue     | Show epilogue and navigate to Credits / Achievements passage
Room         | Play room widget and show sidebar instructions when player needs to present something
Action       | Show action text and navigate back / next to Room unless next action is forced
Verbs        | Verb widgets
Children     | Widgets for regarding the Children of Destiny and their possessions
Palace       | Room and action widgets for Palace region
River        | Room and action widgets for River region
Order        | Room and action widgets for Order region
Chaos        | Room and action widgets for Chaos region
Crypt        | Room and action widgets for Crypt region
Cavern       | Room and action widgets for Cavern region

# Verb widgets

Widget         | Description                  | Invocation                       | Invokes
---------------|------------------------------|----------------------------------|--------
undo           | Implement the UNDO action    | \<\<linkaction undo 'Undo'\>\>   |
(action)       | Set action text              | from buttonaction or linkaction  | goto Action passage
(buttonaction) | Wrap action widget in button | (unused in present version)      |
(linkaction)   | Wrap action widget in link   | from Sidebar buttons and widgets |
regard         | Implement the REGARD action  | <<regard THING [LABEL]>>         | <<regard-THING [LABEL]>>
seize          | Implement the SEIZE action   | <<seize THING [LABEL]>>          | <<seize-THING [LABEL]>>
loot           | Implement the LOOT action    | <<loot THING [LABEL]>>           | <<loot-THING [LABEL]>>
treat          | Implement the TREAT action   | <<treat THING [LABEL]>>          | <<treat-THING [LABEL]>>
present        | Implement the PRESENT action | \<\<present LABEL\>\>            | <<present-$present LABEL>>
smite          | Implement the SMITE action   | <<smite THING [LABEL]>>          | <<smite-THING [LABEL]>>
march          | Implement the MARCH action   | \<\<march LABEL\>\>              | <<march-$room LABEL>>

# Map regions

Region | Rooms
-------|------
Palace | Royal Bedroom, Dining Room, Throne Room
River  | North Bank, Dark River, South Bank
Order  | Path of Order (3)
Chaos  | Path of Chaos (8)
Crypt  | Guard Room, Pit of Darkness, Dark Corridor, Hall of Justice, Crypt of the Sage
Cavern | Cavern of Bones (5)

# Inventory & Children

Topic     | State -1 | State 0        | State 1 | State 2
----------|----------|----------------|---------|--------
conan     | gone     | in room        |         |
loincloth |          | in bed         | worn    |
bottle    | gone     | on table       | closed  | open and empty
vial      |          | in reliquary   | closed  | open and empty
sword     | gone     | on throne      | wielded | broken (hilt)
axe       | gone     | in trophies    | wielded | broken (handle)
ring      |          | in chest       | carried | held by ferryman
necklace  |          | worn by lydia  | carried | held by ferryman
goat      | gone     | in meadow      | carried | in altar
lydia     | gone     | in room        | carried | in altar
alcaz     | gone     | in room        |         |

