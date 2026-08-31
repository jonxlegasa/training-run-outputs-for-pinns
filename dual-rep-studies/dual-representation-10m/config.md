# Dual-representation 10M training configuration

Both representations train on the same canonical ODE indices and minibatches. The power-series and eigenvalue targets are derived from each shared ODE; they are not independently sampled datasets.

- Training ODEs: **10000000**
- Validation ODEs: **500000**
- Final untouched test ODEs: **1000000**
- Batch size: **8192**
- Epochs: **100**
- Global updates per epoch: **1221**
- Global total optimizer updates: **122100**
- Checkpoints: every **5** epochs; the final model is saved separately
- Power-series degree: **N=20** (21 outputs)
- Eigenvalue outputs: **4**
- Models: **2 global + 12 family-specific = 14 total**
- Train dataset ID: `dd0cc9f79584ca627ef80e5339d6c6c48d024bc1c6235a23c61b53de232e9a42`

Validation selects checkpoints. The final test split is evaluated only after the training configuration and checkpoint are fixed.
