# HDL
NOTE: Requires Tensorflow 2 and Keras.
 Modify parameters in config file with the desired values.

To train a basic feed-forward neural network go to ```src``` and execute:
```python train.py --batch_range 64 --network size 256 128 --stab_ratio_range 0.8 --l2 1e-5 --data_set uci10 --train_size 0.8 --lr 3e-4 --val_size 0.2```

To train a stable network, add: ```--is_stable``` and tune ```--stab_ratio_range 0.8```.
E.g., ```python train.py --data_set uci10 --is_stable --stab_ratio_range 0.8```

To train a robust neural network, add: ```-r 1e-3```.

To train a sparse neural network, add: ```--l0 1e-5```.


