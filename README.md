# 2DInfiniteRunner


## Report
My project was to train a DQN controller to play 2DInfiniteRunner Unreal Engine 4 template. 2DInfiniteRunner is a game where you control character by pressing space, which runs along a generic infinite 2D world, and have to jump over enemies and pits for as long as possible. 

The background of the game was removed, fps was set to 32 and resolution to 240x240 for techical purposes, and the game was looped so that after death a new run would start automatically. [UnrealEnginePython](https://github.com/20tab/UnrealEnginePython) plugin was used to connect python code to UE4.

DQN was taken from [FlappyBird](https://github.com/yenchenlin/DeepLearningFlappyBird) due to a high similarity of game process. Before feeding screenshot to the network, they were converted to grayscale and then to black and white colours and then resized to 80x80 using OpenCV. +1 reward was given for successful jump over a pit or an enemy. I also wanted to give -1 reward for death, but at about 1600k tick I noticed that it was not given, because of my misenterpretation of ue blueprints. And though I was sorry, the model trained quite adequately and there were not much time left, so I did not start over :)

Video's length is 1:07. There  are some really nice runs with 5-8 pits passed. However sometimes bot just dives into them.
<img src=https://github.com/vary10/2DInfiniteRunner/blob/master/play.gif>

As we can see the model outperforms random bot.
<img src=https://github.com/vary10/2DInfiniteRunner/blob/master/diagram.png>
I am totally sure, that the model's performance would be much greater, if I made -1 rewards properly:( 

