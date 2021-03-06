<b>SOLVING THE SNAKE GAME WITH Q-LEARNING
by Marouane YALA and Karl BOU ABBOUD</b>


<b>I \ REQUIREMENT :</b>

1 - Pygame : <br>
Download : http://www.pygame.org/download.shtml <br>
Tuto : https://openclassrooms.com/courses/interface-graphique-pygame-pour-python 

2 - PLE (Pygame Learning Environment) <br>
Github : https://github.com/ntasfi/PyGame-Learning-Environment <br>
Doc : http://pygame-learning-environment.readthedocs.io/en/latest/user/home.html

3 - Open AI Gym : <br>
Github : https://github.com/openai/gym <br>
Doc : https://gym.openai.com/docs 

4 - Gym PLE : <br>
Github : https://github.com/lusob/gym-ple <br>
Doc : https://gym.openai.com/envs/Snake-v0


<b>II \ SNAKE GAME :</b>

Snake is a game where the agent is a snake who has to eat the food appearing in the screen.
The food appears randomly in the window. Each time the snake eats, its tail grows in
length. The tail follows exactly the lead of the head.

<b>Rules :</b> <br>
Th rules of the snake game are as followed : <br>
– Actions : Up, down, left and right. The snake can not turn back on itself (for instance,
he can’t go left if he’s already going to the right). <br>
– Final States : The games ends if the agent eats all the food on the screen (it’s the
win scenario, the snake occupies all the space on the screen), or if the snake comes in
contact with its tail (game over scenario). <br>
– Rewards : The agent receives a positive reward when he eats, a negative reward when
he enters in contact with his body.


<b>III \ MODELISATION PLANNED :</b>

<b>Environment :</b> <br>
One of the most famous environment for the snake game is the PyGame Learning Environment
(PLE). It is a learning environment, mimicking the Arcade Learning Environment
interface, allowing a quick start to Reinforcement Learning in Python. The goal of PLE is
allow practitioners to focus design of models and experiments instead of environment design,
which is exactly what we need. <br>
The size of the state space being huge, due to the various possible positions of the snake’s
body, we will use a neural network which, given a certain state, predicts the Q function for
each respective action. We will use Keras libraries. <br>
In addition, we will use Open AI Gym’s toolkit to develop and compare our reinforcement
learning algorithms, which is compatible with famous numerical computation
library such as TensorFlow or Theano used with Keras (high level neural networks library
for Python), and is compatible with PLE’s snake environment since about a month.

<b>Modelisation :</b> <br>
- Q-Learning : implementing a classic Q-Learning off-policy approach and observe its
limits. <br>
- TD(lambda) : in a second-time, we combine Q-Learning with eligibility traces to obtain
more general models, and compare performance.


<b>IV \ ALGORITHMIC APPROACH :</b>

As stated above, we will base our research on a snake environment provided by PyGame
Learning Environment and Open AI Gym. We will build a Q-Learning Agent, a Q(lambda) agent
using a Neural Network powered by Keras libraries to predict the Q-function, and compare
their performance.