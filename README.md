Download Link: https://assignmentchef.com/product/solved-cs285-assignment-1-imitation-learning
<br>
The goal of this assignment is to experiment with imitation learning, including direct behavior cloning and the DAgger algorithm. In lieu of a human demonstrator, demonstrations will be provided via an expert policy that we have trained for you. Your goals will be to set up behavior cloning and DAgger, and compare their performance on a few different continuous control tasks from the OpenAI Gym benchmark suite. Turn in your report and code as described in Section 4.

The starter-code for this assignment can be found at <a href="https://github.com/berkeleydeeprlcourse/homework_fall2019">https://github.com/berkeleydeeprlcourse/ </a><a href="https://github.com/berkeleydeeprlcourse/homework_fall2019">homework_fall2019</a><a href="https://github.com/berkeleydeeprlcourse/homework_fall2019">.</a> Follow the instructions in the Readme file to setup the codebase.

<h1>Section 1.    Behavioral Cloning</h1>

<ol>

 <li>The starter code provides an expert policy for each of the MuJoCo tasks in OpenAI Gym. Fill in the blanks in the code marked with Todo to implement behavioral cloning. A command for running behavioral cloning is given in the Readme file.</li>

</ol>

The following files have blanks in them and can be read in this order:

<ul>

 <li>scripts/run hw1 behavior cloning.py</li>

 <li>infrastructure/rl trainer.py</li>

 <li>agents/bc agent.py</li>

 <li>policies/MLP policy.py</li>

 <li>infrastructure/replay buffer.py</li>

 <li>infrastructure/utils.py</li>

 <li>infrastructure/tf utils.py</li>

</ul>

<ol start="2">

 <li>Run behavioral cloning (BC) and report results on two tasks: one task where a behavioral cloning agent achieves at least 30% of the performance of the expert, and one task where it does not. When providing results, report the mean and standard deviation of the return over multiple rollouts in a table, and state which task was used. Be sure to set up a fair comparison, in terms of network size, amount of data, and number of training iterations, and provide these details (and any others you feel are appropriate) in the table caption.</li>

</ol>

Tip: to speed up run times, the video logging can be disabled by setting –video log freq -1

<ol start="3">

 <li>Experiment with one set of hyperparameter that affects the performance of the behavioral cloning agent, such as the number of demonstrations, the number of training epochs, the variance of the expert policy, or something that you come up with yourself. For one of the tasks used in the previous question, show a graph of how the BC agent’s performance varies with the value of this hyperparameter, and state the hyperparameter and a brief rationale for why you chose it in the caption for the graph.</li>

</ol>

<h1>Section 2.    DAgger</h1>

<ol>

 <li>Implement DAgger by filling out all the remaining blanks in the code marked with Todo. A command for running DAgger is provided in the Readme file.</li>

 <li>Run DAgger and report results on one task in which DAgger can learn a better policy than behavioral cloning. Report your results in the form of a learning curve, plotting the number of DAgger iterations vs. the policy’s mean return, with error bars to show the standard deviation. Include the performance of the expert policy and the behavioral cloning agent on the same plot. In the caption, state which task you used, and any details regarding network architecture, amount of data, etc. (as in the previous section).</li>

</ol>