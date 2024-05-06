# A3C-for-Kung-Fu

## Description
You are a Kung-Fu Master fighting your way through the Evil Wizard’s temple. Your goal is to rescue Princess Victoria, defeating various enemies along the way. The agent is trained using the A3C algorithm. The A3C algorithm gives the agent critical thinking.

## Preview 

https://github.com/CoboAr/A3C-for-Kung-Fu/assets/144629565/4ffd9c10-e731-4695-9063-10293e9e9d1b

## Requirements 
 Google Colab       
 [Gymnasium Documentation Kung Fu](https://gymnasium.farama.org/environments/atari/kung_fu_master/)      
 PyTorch

 ## How does A3C algorithm work?

 The Asynchronous Advantage Actor-Critic (A3C) algorithm is a reinforcement learning algorithm that combines the advantages of actor-critic methods with asynchronous training. 
 It's designed to efficiently learn policies for sequential decision-making tasks, such as playing video games or controlling robotic systems. Here's how it works:
 <ol>
   <li>Actor-Critic Architecture:</li>
   <ul>
     <li>The A3C algorithm is based on the actor-critic architecture, which consists of two components:</li>
     <ul>
       <li>Actor: The actor is responsible for selecting actions given the current state. It learns a policy that maps states to actions. In A3C, the actor is typically implemented as a neural network that takes states as input and outputs a probability distribution over actions.</li>
       <li>Critic: The critic evaluates the value of state-action pairs. It learns to estimate the expected return (cumulative reward) from taking an action in a given state. In A3C, the critic is also implemented as a neural network that takes states as input and outputs state values.</li>
     </ul>
   </ul>
   <li>Asynchronous Training:</li>
   <ul>
     <li>A3C introduces asynchronous training to parallelize the learning process across multiple actor-learner agents (threads). Each agent runs a copy of the environment and interacts with it independently.</li>
     <li>During training, each agent collects experiences by interacting with its own copy of the environment and updates its local actor and critic networks based on these experiences.</li>
     <li>Asynchronous updates allow for more efficient exploration of the state-action space and help prevent the agents from getting stuck in local optima.</li>
   </ul>
   <li>Policy and Value Function Updates:</li>
   <ul>
     <li>During training, the actor and critic networks are updated using a combination of policy gradient and value function methods.</li>
     <li>The actor's policy is updated to increase the likelihood of actions that lead to higher returns (as estimated by the critic), while decreasing the likelihood of actions that lead to lower returns.</li>
     <li>The critic's value function is updated to better estimate the expected return from different states, based on the observed rewards and estimated advantages.</li>
   </ul>
   <li>Asynchronous Parameter Sharing:</li>
   <ul>
     <li>A3C implements asynchronous parameter sharing, where each agent has its own copy of the neural network parameters (weights) but periodically shares its updates with a global network.</li>
     <li>By asynchronously sharing updates, A3C facilitates communication between agents and allows them to benefit from each other's experiences without the need for centralized coordination.</li>
   </ul> 
 </ol>

Enjoy! And please do let me know if you have any comments, constructive criticism, and/or bug reports.
## Author
## Arnold Cobo
