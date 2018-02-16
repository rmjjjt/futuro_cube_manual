# Score

Display and announce reached score

Syntax: `Score(score, flag = SCORE_NORMAL, voice = 1, double_tap = 1)`

* `score` actual score to display <0...999>
* `flag` score color version type from SCORE definition
  - `SCORE_NORMAL` blue score - middle range
  - `SCORE_WINNER` colorful score - high range
  - `SCORE_LOSER` red score - low range
* `voice` if set to 1, score is announced
* `double_tap` if set to 1, function is waiting for double tap to restart and also voice ”double tap to restart the game” is announced

Notes: This function draws the score on the cube without using the standard drawing method. 
It is recommended to use it at the end of a game without any other drawing. 
Color scheme is selected by score definition type. 
It can announce the score by voice and it also can wait for a double tap to restart the game. 
To draw the score in the standard way, see [DrawScore](drawscore.md).

Example:

* `Score(199)` draw 199 in NORMAL colors, announces the score and waits for double tap