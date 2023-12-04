## Abhishek Shankar (ashankar1@stevens.edu)

### https://github.com/AbhishekShankar17/AdventureGame

1. Time spent: Spent about 9 - 11 hours on the design, map and coding part of the project. 

2.  Testing:


    * I conducted hands-on testing for any glitches in the code and utilized doctests as well. To ensure alignment with transcripts, I employed a diff checker.

    * 3 must keys which are name, desc and exits.
    
    * Conducted initial tests on a compact dataset consisting of 4-5 rooms, including items in select rooms, to verify the functionality of dropping and retrieving items. Subsequently, this was expanded to a larger dataset for further testing.
    
    * Tested exits if empty that it goes no where.


3. Unresolved Bugs 

    * It's noted that when only directional abbreviations are typed, the system functions flawlessly. However, it encounters issues when these abbreviations are used in conjunction with verbs. This aspect can be considered for enhancement in future updates.
    
    * Exits have to be in dictionary data structure, lists data structures would not be handled.
    
    * If the exits are not in lowercase, there will be a mismatch with the predefined keys, causing a break.

4. Resolved Bugs

    * Initially, I directly embedded the verbs into the code, but I later transitioned to utilizing a helperVerbs.py file. This approach simplifies tracking and managing the verbs, allowing for seamless future enhancements and modifications (this represents more of an enhancement rather than a fix for a bug).
    
    * Wrote a more efficient way of calling processes dynamically
    
    * Also used getters and setters for better improvement
    
    
5. The three implemented extentions are:


      -The drop extention
      
      The drop extension drops the particular item which is picked, its the opposite of get verb.

      ##### Usage 

      ```

      $python3 adventur.py loop.map
    > A white room

    You are in a simple room    with white walls.

    Exits: north east

    Items: rose, ball, caps, 

    What would you like to do?  get ball
    You pick up the ball.
    What would you like to do?  drop ball
    You drop the ball
    > A white room

    You are in a simple room    with white walls.

    Exits: north east

    Items: rose, caps, ball, 

    What would you like to do?  quit
    Goodbye!
    ```


    -The Directions and Abbreviations extention


    In this enhancement, participants can now navigate by inputting directions directly as commands. In the earlier version, typing a direction alone would cause an error because it required preceding the direction with the "go" verb. But with this new update, users have the convenience of moving in any chosen direction by merely entering the direction as the command.
    The Abbreviations are commpletely written in helperVerbs.py as instead of core functionality in adventure.py. I have added helpersVerbs.py which helps code look clean.


    ##### Usage
    ```
    $ python3 adventure.py loop.map
    > A white room

    You are in a simple room with white walls.

    Exits: north east

    Items: rose, ball, caps, 

    What would you like to do? s
    There's no way to go south.
    What would you like to do? e
    You go east.

    > A red room

    This room is fancy. It's red!

    Exits: north west

    Items: rose, 

    What would you like to do? n
    You go north.

    > A green room

    You are in a simple room, with bright green walls.

    Exits: west south

    What would you like to do? quit
    Goodbye!
    ```

    -The help Extension 
    
    The 'help' verb informs players about the allowed verbs. For verbs that anticipate a specific target, we add '...' following them.

    ##### Usage
    ```
    % python3 adventure.py sample.json
    > Emerald Forest

    You find yourself amidst towering trees with light filtering through the leaves.

    Exits: east south

    Items: enchanted bow, mysterious rune, 

    What would you like to do? help
    You can run the following commands:
    go ...
    get ...
    look
    inventory
    quit
    help
    drop ...
    ```



      




