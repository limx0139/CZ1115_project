# CZ1115_project





## Project Details

This is a student project for one of the more decent modules at Nanyang Technological University, a research university based in Singapore.
The objective of the project is to utilise machine learning(ML) to find relationships between chess openings and win rates across different player strength. We aim to find a correlation between player strength, that is their prowess on the board, the opening few moves played in a game, and how likely it is for them to win said game.

We make use of the following dataset:
https://web.chessdigits.com/data
where the author, Patrizsche, https://lichess.org/@/Patrizsche, has corroborated from the lichess database, which is a database of online chess games played on Lichess, one of the biggest online chess websites in the world.

## Common Chess Terminology used in this Project

    White: Player with white colored pieces, starts first
    Black: Player with black colored pieces, starts second
    Center: Center of the board, most openings feature both sides aggressively competing for the center squares.
    Opening: First few moves, given a name by some guy who reportedly pioneered/popularised it
    Rating/ELO: Relative strength of an individual player. For this project, we take below 1200 is low, 1200 to 1800 as mid and above 1800 as high rating. For reference, chess grandmasters nowadays have a rating of around 2500, with the best in the world at 2800 to 2900, the chess engine Stockfish on the other hand, has a rating of over 3800.
        Types of Opening:
            Attack: Generally White actively pursues an offensive opening
            Defense: Opening characterised by Black's unique moves to mount a defense
            Opening: Opening characterised by white's first move
            Gambit: Opening characterised by material sacrifice for some sort of compensation, usually piece development
        Notable Openings:
            Sicilian Defense:
                1.e4 c5
                Most popular game in the dataset, known to provide equal opportunities to both sides at higher levels.
            Philidor's Defense:
                1.e4 e5, 2.Ng3 e6
                Considered solid for black before the age of engines, now considered terrible for black
            Van't Kruij's Opening:
                1. e3
            Modern Defense:
                1. ... g6
                Popularised by chess engines, developing the flank rather than center, going against chess theory, to go for the center, perfectly holdable in theory.
    Strength(rating): The state of having a higher ELO rating than one's opponent, which translates to being statistically the better player, hence more likely to win.
    Time Control: How much time each player is allowed to use to think/play their moves. Running out of time results in a time forfiet, they lose by default, with some exceptions that are not relevant to this project.
    Types of time control:
        Bullet: The shortest time control, typically 1 minute per player.
        Blitz: Typically 3 minutes per player, though can be as long as 5.
        Rapid: 10 to 30 minutes per player
        Classical: Very long, likely the most prestigious time format, players can take hours for their moves. Generally played by very good chess players.
    Winrate: A measure of how successful one is at winning, calculated by # of wins / total games played
    Win: Checkmating the opposing king(not relevant as we are mainly concerned about opening strategy) or having the opponent forfiet on time.
    Evaluation: Engine(generally Stockfish) evaluation of a position, measured by an Interval scale with 0 as balanced(draw) and positive or negative scores favoring white or black respectively.
    Not as relevant in this context as openings generally do not have that great an evaluation disparity.
    Advantage/winning position: A position, that given near perfect play on both sides, likely ends with one side victorious. For engines, a evaluation disparity of 1 may be winning but humans, generally only consider a position winning with 2 to 3.

    
    

## Why some openings are more frequent than others
    1. Popularity
        Players like to stick to openings they are familiar with
    2. Ease of getting to the opening(# of moves before the opening is 'officially' on the board)
        ie. most openings are reached in the first 2 moves, 2 white moves, 2 black moves, but some may be reached in 1, making them more frequent
    3. Relative advantage of each side
        While chess is generally thought to be a balanced game, openings may not be. Though white has an inherrent advantage(both theoratically with the advantage of the first move, and statistically, that white wins more by a few percentages overall), some openings give one side a very large advantage, leading to a disproportionately high winrate, even accounting for white's advantage, and as a result are generally avoided by better players.

## Our Expectations
    We expect uwu the opening to play a much stronger role in deciding the game for lower rated games as well as shorter time controls than otherwise as we believe, stronger players will be able to choose the right openings that do not give their opponent too much of an advantage, and that as time control increases, move accuracy would also increase, reducing the possible advantage gained in the opening.

For each bracket, we wish to find an optimal opening for each side, characterised by relative ease to achieve and relatively high winrates.

## Methodology:
We split the dataset into categories, based on the players' average rating and the time control of a game. Then, for each dataset, we find the average win rates for each opening for white and black, and plot a classification graph on the dataset so see how the former would hold up down the classification tree. That is, we analyse what openings players tend to choose given the disparity in their strength relative to their opponent and how their choice plays out for them. While we did perform the analysis for all the categories we made, the format of the project meant that we would focus on two categories in particular, the blitz time control compared to the general dataset.






