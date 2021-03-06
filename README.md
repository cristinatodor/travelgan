# Image-to-image domain translation using TraVeLGAN

PyTorch implementation of [TraVeLGAN: Image-to-image Translation by Transformation Vector Learning](https://arxiv.org/abs/1902.09631).

Add configuration file and run with :

```
python train.py --hparams=config_file --log=/runs/exp --device={0,1,..}
```

You can run the training of TraVeLGAN between two classes of CIFAR10 dataset using the ```cifar.json``` file. Download the dataset into the ```data``` folder and run the command above.


Here is an example with bird-ship (32x32) translation after 500 epochs.

![bird](./samples/bird.png)
![bird_ship](./samples/bird_ship.png)

![ship](./samples/ship.png)
![ship_bird](./samples/ship_bird.png)


Here is an example with rock beauty-toucan (128x128) translation after 10k iterations (batch size 16).

![bird](./samples/toucan.png)
![bird_ship](./samples/toucan_rockbeauty.png)

![ship](./samples/rockbeauty.png)
![ship_bird](./samples/rockbeauty_toucan.png)


As a side note, I could not reproduce results (persistent mode collapse) without spectral normalization.
