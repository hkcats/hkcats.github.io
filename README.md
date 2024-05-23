# Sequence (h's Version)
An online multiplayer version of the board game Sequence


## Notes for future me:
- i think hardcoding the board(s) would be better? def not gonna server it
    - means boards & lib will probs be deleted; should edit json to match
- seperate internal rep vs drawing it vs client
- i think a state machine might work, rather than async? look into it tho
- will github page automatically run w typescript? aka no need to run client, etc?
    - how's that work for multiplayer?? research
- try single player version first, up to 3 people ig? then later implement team version

## For Now:
- playing a one-eyed jack on an empty board may break game/skip players turn/something bad
- ^ same may occur for running out of cards
- board, colors, all set as variables
- solo player only, up to three (tho idk if theres actually a limit ig)

## Rules:

### Setup
1. Deck Shuffled & `6` cards dealt per `3` players
2. Board layed out & no tokens
3. Each player assigned `color`

### Player Turn
1. Choose 1 Card in Hand
    - if one-eyed jack and empty board: deselect and _restart turn_.
    - if dead card: discard, draw again, and _restart turn_.
2. Choose 1 Tile on Board
    - if jack:
        - one-eyed: if tile w token, remove token
        - two-eyed: if tile w/o token, add token
           - if board now filled, _end game_.
    - if reg and tile w/o token, add token
           - if board now filled, _end game_.
    - finally:
        - discard card
        - draw new card
            - if no cards left, _end game_
   

















