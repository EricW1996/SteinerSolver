# SteinerSolver

Code and some dataset for SteinerSolver.

SteinerSolver is a deep reinforcement learning model to solve Euclidean Steiner tree problem.

## File
/attention_completeV1.3.1 is the code for the deep reinforcement learning model.

/steiner tree experiment data includes the dataset and the corresponded minimal Steiner tree.

## Paper

## Model

![Encoder model](https://github.com/cdslabamotong/SteinerSolver/blob/main/attention_completeV1.3.1/encoder.png?raw=true)

![Decoder model](https://github.com/cdslabamotong/SteinerSolver/blob/main/attention_completeV1.3.1/decoder.png?raw=true)

## Dependencies
 *   Python>=3.8
 *   NumPy
 *   SciPy
 *   PyTorch>=1.7
 *   tqdm
 *   tensorboard_logger
 *   Matplotlib (optional, only for plotting)
## Usage
### Train
For training Steiner tree poblem instances with 10 nodes and using rollout as REINFORCE baseline
```bash
python run.py --problem tsp --graph_size 10 --batch_size 32 --epoch_size 10240 --val_size 10000 --eval_batch_size 10 --baseline rollout --run_name 'st20_rollout' --n_epochs 100 --lr_model 0.00005 --seed 1111 --embedding_dim 128 --hidden_dim 128 --n_encode_layers 5 --load_path epoch-98.pt
```

## Acknowledgements
Thanks to [wouterkool/attention-learn-to-route](https://github.com/wouterkool/attention-learn-to-route#attention-learn-to-solve-routing-problems) for getting me started with the code for the attention model.
