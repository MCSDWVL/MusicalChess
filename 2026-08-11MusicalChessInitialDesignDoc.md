# Musical Chess
Musical Chess is a game where users craft songs to control the movement of chess pieces.

# Goals
- Users feel like they are creating songs worthy of listening to again and sharing with friends/strangers.
- Users do not need to have any musical talent, rather the song is a byprodcut of play
- Play feels strategic and interesting
- Mechanics feel familiar and intuitive

# Mechanics
Play takes place on a steady rhythm.

On each "beat", one piece is active to "receive" the command from a note. This can be a white (player) or opponent (black) piece.

When a piece is active, the note played determines the behavior. Obviously some pieces have more options than others - pawns 
can only handle a single note, while other pieces have much more complex handling.

For a piece that takes a direction and a distance, like a castle, bishop, or queen, they should consume two beats - the first
note sets the direction, and the second node adds distance. If the second beat is empty they can just move a single space.

For a piece like a pawn that can only take limited actions, we should collapse to a valid "move forward" action when nothing else
is available. For other pieces with many options, if they select a move that is invalid (like moving into a wall) it should just be dropped.
However if a move attempts to move "too far" because a collision with a wall or other piece happens, it should just move as far as possible.

Pawns should become queens when reaching the opposite side of the board.

# How users enter notes
This area is to-be-determined and we should expect to prototype many layers. Users should not have to select "C#", rather
they should have a palette that fits the key and guarantees reasonably harmonic outcomes.

For version one, we should plan every N measures to allow the user to enter a new note in any "slot" they want.

The notes should cover all possible moves, so we would need 8 directions for a queen or king or knight, and up to 8 for distance.

# End of Play
Play ends when all pieces on one side are eliminated, NOT when a king is checkmated.

After play ends, there should be a "replay" option that plays back the song without the interruptions of pausing for user input, so that users
can get a feel for the song they created and how it escalated over time.

# Start of Play
Pieces should be randomly added to the board - we should NOT start with a standard chess setup.

We may also consider starting with a board that is not 8x8, TBD as we experiment.
