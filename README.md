# PyTorch implementation of TRPO

Try my implementation of [PPO](github.com/ikostrikov/pytorch-a2c-ppo-acktr/) (aka newer better variant of TRPO), unless you need to you TRPO for some specific reasons.

##

This is a PyTorch implementation of ["Trust Region Policy Optimization (TRPO)"](https://arxiv.org/abs/1502.05477).

This is code mostly ported from [original implementation by John Schulman](https://github.com/joschu/modular_rl). In contrast to [another implementation of TRPO in PyTorch](https://github.com/mjacar/pytorch-trpo), this implementation uses exact Hessian-vector product instead of finite differences approximation.

## Contributions

Contributions are very welcome. If you know how to make this code better, don't hesitate to send a pull request.

## Usage

```
python main.py --env-name "Reacher-v1"
```

## Recommended hyper parameters

InvertedPendulum-v1: 5000

Reacher-v1, InvertedDoublePendulum-v1: 15000

HalfCheetah-v1, Hopper-v1, Swimmer-v1, Walker2d-v1: 25000

Ant-v1, Humanoid-v1: 50000

## Results

More or less similar to the original code. Coming soon.

## Todo

- [ ] Plots.
- [ ] Collect data in multiple threads.

opperVrepEnv: initialized
('lagrange multiplier:', tensor(0.9463), 'grad_norm:', tensor(0.1324))
fval before 7.234932567316675e-16
a/e/r 0.018974816855454022 0.01892691153492239 1.0025310690781875
fval after -0.018974816855453297
Episode 1	Last reward: 236.81292313337326	Average reward 216.06
('lagrange multiplier:', tensor(1.1607), 'grad_norm:', tensor(0.1293))
fval before 2.221492916534599e-17
a/e/r 0.027238908095333494 0.0232143024365327 1.1733675034950526
fval after -0.027238908095333473
Episode 2	Last reward: 494.25662350840867	Average reward 237.87
('lagrange multiplier:', tensor(1.1492), 'grad_norm:', tensor(0.1489))
fval before -2.854710458782077e-18
a/e/r 0.026381655786859668 0.022984507304948745 1.1478016664372654
fval after -0.02638165578685967
Episode 3	Last reward: 384.5887573957443	Average reward 265.76
('lagrange multiplier:', tensor(1.1970), 'grad_norm:', tensor(0.1930))
fval before -3.4907139064255345e-17
a/e/r 0.02622897300476402 0.02393942355394439 1.0956392891274274
fval after -0.026228973004764056
Episode 4	Last reward: 109.77745985984802	Average reward 295.63
('lagrange multiplier:', tensor(1.1487), 'grad_norm:', tensor(0.1985))
fval before 3.8131426583991645e-17
a/e/r 0.02435699490955636 0.022974102126439713 1.0601935507862632
fval after -0.024356994909556322
Episode 5	Last reward: 474.0409964323044	Average reward 334.85
('lagrange multiplier:', tensor(1.0177), 'grad_norm:', tensor(0.1965))
fval before 9.676075978881781e-17
a/e/r 0.020612294595517094 0.020354220952038198 1.012679121646906
fval after -0.020612294595516997
Episode 6	Last reward: 433.3781426548958	Average reward 377.08
