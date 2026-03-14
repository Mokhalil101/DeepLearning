
### Monte Carlo vs SARSA vs Q-Learning

This section compares three fundamental **model-free reinforcement learning algorithms** and explains how each one learns and updates its knowledge.



###  Monte Carlo

Monte Carlo learning updates its values **after the entire episode is completed**.  
The agent interacts with the environment until it reaches a terminal state, then updates the Q-values using the **total accumulated return**.

**How it learns:**
- Collects all (state, action, reward) pairs in an episode
- Waits until the episode ends
- Updates Q-values based on total return

**Key points:**
- Episode-based learning
- Requires terminal states
- Simple but slow learning
- High variance, stable results



### SARSA (On-Policy Learning)

SARSA is an **on-policy temporal-difference** algorithm.  
It updates Q-values **at every step** using the **actual action taken** by the current policy (including exploration).

**How it learns:**
- Learns while interacting with the environment
- Uses the next selected action for learning
- Follows the same policy for learning and acting

**Key points:**
- Step-by-step learning
- On-policy
- More conservative and safer behavior
- Suitable for real-world and risky environments



###  Q-Learning (Off-Policy Learning)

Q-Learning is an **off-policy temporal-difference** algorithm.  
It learns the **optimal policy** by updating Q-values using the **maximum possible future reward**, regardless of the action actually taken.

**How it learns:**
- Learns during interaction
- Uses the best possible next action for update
- Learns independently of the behavior policy

**Key points:**
- Step-by-step learning
- Off-policy
- Faster convergence
- More aggressive exploration

