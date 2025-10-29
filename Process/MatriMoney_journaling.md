This journal is for jotting down my thinking and decision making when I am actively working on *Matri-Money*.

<p align="center">*October 27, 2025*</p>

**Intention**
Over the course of the first couple of days of working on *Matri-Money*, I wanted to create a basic "game board" in Twine. 

**Log**
- The first (incomplete) version of this prototype that I uploaded was a 40-space digital game board that represents players' commute from home to work. (40 spaces is 1/4 the number of spaces on the *GoL* board.)
- I created a few variables ($Cash, $Spouses, $Kids) and stored them in the launchpoint passage. I also made a variable to track players' rolls using the game's spinner ($d10). 
- Players start with $50.00 in cash, something I'll likely adjust later. 
- The spinner is actually a series of spinners: For each space, there's an associated spinner space (e.g., Space 1 and S1 Spinner). The spinner uses a macro that selects a random number between 1 and 10 like the physical spinner *GoL*. 
- I arranged the 40 spaces in a spiral and added starting space on the outside, as well as a final space in the center called "Finish!/Work."
- I populated the first 10 spaces with writing describing various situations where players lose money, gain money, gain spouses, etc., and programmed the corresponding changes to different variables.
- Between spaces 1-10, every third space is a Spouse Space. I wanted players to have relatively high chance of getting married early on in the (relatively short) journey

**Reflection**   
I realize now that visually, this design is significant departure from a table-top board gaming experience where you can see the entire play space, including the finish line and your competitor's position relative to your own. Because I chose to use Twine, players can only see what's happening on the space they currently occupy. 

I think there are pros and cons here: On the one hand, being able to see the finish line and one's positiion on the "board" relative to competitors might lead to an increased sense of competition; On the other hand, players having to communicate with one another to take turns spinning and moving could lead to new possibilities. 

What I've made here can only be played by one person per device, so multiplayer use requires players being on their devices and going on parallel commutes. Players will need to communicate "*Battleship*"-style rather than having turn-taking enforced by Twine code. What can I *do* with that? 

&nbsp;
&nbsp;
<p align="center">*October 28, 2025*</p>

**Intention**
Today, I want to finish adding spinners to the remaining spaces and add the remaining Spouse Spaces to the board. 

**Log**
- I added spinners to spaces 11-40. 
- I realized that players couldn't see changes in the variables as they happened (e.g., if they got married on Space 3, they wouldn't see a spouse added to their count until their next turn) so I stored the variables directly in the spaces themselves rather than their corresponding spinners.
- I continued writing instructions for other spaces where players gain and lose money.
- At least for now, I decided that players will gain money in very small increments ($1.00, $3.00, $5.00, $10.00) and risk losing higher amounts ($5.00, $10.00, $15.00, $25.00) so that losses feel significant and gains made by marrying/having kids
are the most efficient way to accumulate enough wealth to win. 
- I changed the intro text to reflect a more suitable value for kids since a number in the thousands felt a bit high ($50.00)
- I added Spouse Spaces to the rest of the board. (Total: 12/40)
- Between spaces 1-15, every third space is a Spouse Space. After that, they are distributed across the board at varying concentations that can reflect different situations/encounters on the players' commutes 
- I tagged all Spouse Spaces and colour coded them purple. 
- I added a two spaces where you can marry a couple. 
- I added one space right before the finish line where you get an additional Baby Bonus at the end for having a partner who is already pregnant. 

**Next Up**
- Right now, Spouse Spaces all say the same thing ("It's your lucky day! You fall in love and get married!"). This feels kind of boring. I would like to write a variety of descriptions for each of these if I can, as well as for spaces where you lose a spouse. 
- Finish populating other spaces with descriptive text
- Add a few Annulment spaces that cause players to lose spouses (which introduces an element of risk)
- Figure out how to do the final count and end the game
- Playtest note: Should there be more spouse spaces? Fewer?; What should I change about wealth accumulation (how often, in what amounts)?

**Ideas**
- Someone left a comment in my Discord journal suggesting a secondary win condition: If spouses could independently marry each other, then the game could end if/when everyone is married each other; Additionally, play could become cooperative if players marry into the same network. I think this is worth exploring down the line! I was already thinking about cooperative what cooperative versions of this game would look like, and I'm interested in what it could look like to have a dynamic combination of competition and collaboration...
- In future iterations, it could be interesting to see what happens if players have to re-invest their money back into maintaining their marriages or else risk losing them. Families have no cost in *GoL*, so what happens if we introudce one?
- In future iterations, I would like to try to make it so that landing on the same space means marrying *the same* spouse. 
- If I were to continue having children be worth thousands of dollars such that other spaces affecting the $Cash variable become flavourtext, maybe those little story beats could carry variables that change the end-state/ win condition? 
- What if there were a secondary spinner that determined *how many* partners you gain when you get married? (A single person, a couple, a triad, a whole polycule of 4+ people?)


**Reflection**
- Feeling: Intimidated by Godot, excited that the core spinner/movement mechanic is working
- The fact that I am not an experience programmer meant that I didn't know how to store variables in a way that let me use a single spinner and ended up creating multiple spinners that each connect to all possible rolls. In combination with the board's shape, this created a really interesting flow or arrows on the Twine interface (see the folder labeled "Images - Prototype Screenshots"). 
- Re: lowering the value of each kid from $5000.00 to $50.00 - was there something funny about having the children be worth a ludicrous amount? Do I want this back? When the value is that high, the spaces where players win/lose money basically turn into flavourtext. I could at least make it so that these little story beats change something at the end of the game...
- The decision to included a Baby Bonus for having a partner who is already pregnant kind of touches on the relationship between compulsory hetero-monogamy and capitalism: Here, the idea that the child is not a part of the family line/the line of property inheritance is not a threat, it's a good thing! 

Here are two screenshots showing a visualization of the differences between the first and second pass on Twine: 

[Twine screenshot - MatriMoney_V1a_screenshot1](<Process/Images/Images - Prototpye Screenshots/MatriMoney_V1a_screenshot1.png>)   

[Twine screenshot - MatriMoney_V1b_screenshot1](<Process/Images/Images - Prototpye Screenshots/MatriMoney_V1b_screenshot1.png>)

