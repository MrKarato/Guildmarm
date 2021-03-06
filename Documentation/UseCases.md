|Use Case 1|Querying for monster description|
|---|---|
|**Related Requirements**|Req 1, Req 9|
|**Initiating Actor**|User|
|**Participating Actors**|StringValidator, Database|
|**Preconditions**|There is a monster to query the database for.|
|**Postconditions**|User is given a description for the monster they asked for.|
|**Flow of Events for Main Success Scenario**||
|1.|User inputs query in form  "!monsterdesc -Monster Name-".|
|2.|Guildmarm parses string, verifies there are no mistakes in the name.|
|3.|Guildmarm queries the server for the monster's description.|
|4.|Guildmarm replies to the user with the description.|
|**Flow of Events for Alternate Scenarios**||
|2a.||
|1.|Guildmarm detects an error in the string.|
|2.|Guildmarm replies to the user detailing the error.|
|3a.||
|1.|The server has no monster with the given name.|
|2.|Guildmarm replies to the user, informing them that no such monster is recorded.|
|3b.||
|1.|The monster has no description.|
|2.|Guildmarm replies to the user, informing them that the monster has no description.|

|Use Case 2|Querying for monster's parts|
|---|---|
|**Related Requirements**|Req 1, Req 5, Req 9|
|**Initiating Actor**|User|
|**Participating Actors**|StringValidator, Database|
|**Preconditions**|There is a monster to query the database for.|
|**Postconditions**|User is given a table of the monster's part drops.|
|**Flow of Events for Main Success Scenario**||
|1.|User inputs query in form  "!monsterparts -Monster Name-".|
|2.|Guildmarm parses string, verifies there are no mistakes in the query.|
|3.|Guildmarm queries the server for the monster's part list.|
|4.|Guildmarm replies to the user with a table of the monster's parts.|
|**Flow of Events for Alternate Scenarios**||
|2a.||
|1.|Guildmarm detects an error in the string.|
|2.|Guildmarm replies to the user detailing the error.|
|3a.||
|1.|The server has no monster with the given name.|
|2.|Guildmarm replies to the user, informing them that no such monster is recorded.|
|3b.||
|1.|The monster has no parts.|
|2.|Guildmarm replies to the user, informing them that the monster has no parts data.|

|Use Case 3|Querying for monster's elemental weaknesses and a recommendation|
|---|---|
|**Related Requirements**|Req 1, Req 4, Req 9|
|**Initiating Actor**|User|
|**Participating Actors**|StringValidator, Database|
|**Preconditions**|There is a monster to query the database for.|
|**Postconditions**|User is given a weapon recommendation and location to focus.|
|**Flow of Events for Main Success Scenario**||
|1.|User inputs query in form "!monsterrecc -Monster Name-".|
|2.|Guildmarm parses string, verifies there are no mistakes in the query.|
|3.|Guildmarm queries the server for the monster's elemental weaknesses list.|
|4.|Guildmarm calculates what the best element to bring would be.|
|5.|Guildmarm replies to the user with a weapon recommendation recommendation and location to focus.|
|**Flow of Events for Alternate Scenarios**||
|2a.||
|1.|Guildmarm detects an error in the string.|
|2.|Guildmarm replies to the user detailing the error.|
|3a.||
|1.|The server has no monster with the given name.|
|2.|Guildmarm replies to the user, informing them that no such monster is recorded.|
|3b.||
|1.|The monster has no elemental weaknesses.|
|2.|Guildmarm replies to the user, informing them that the monster has no elemental weakness data.|

|Use Case 4|Querying for item drop locations|
|---|---|
|**Related Requirements**|Req 1, Req 2, Req 5, Req 9|
|**Initiating Actor**|User|
|**Participating Actors**|StringValidator, Database|
|**Preconditions**|There is an item to query the database for.|
|**Postconditions**|User is given a list of the possible locations they can obtain the part.|
|**Flow of Events for Main Success Scenario**||
|1.|User inputs query in form "!itemsearch -Item Name-".|
|2.|Guildmarm parses string, verifies there are no mistakes in the query.|
|3.|Guildmarm queries the server for the full list of monsters and quests.|
|4.|Guildmarm calculates searches through the list for the item.|
|5.|Guildmarm replies to the user with a list of the potential drop sources.|
|**Flow of Events for Alternate Scenarios**||
|2a.||
|1.|Guildmarm detects an error in the string.|
|2.|Guildmarm replies to the user detailing the error.|
|4a.||
|1.|The list does not contain the item being searched for.|
|2.|Guildmarm replies to the user, informing them that no item is recorded.|