# localization-app

`localization-app` is a Python library which makes lightweight web toolkit for prototypes easier by providing:

* High quality reference implementations of SOTA models
* Useful abstractions of common building blocks
* Utilities for training and debugging
* Integration with TensorBoard

## Installation

To install `localization-app`, clone and install requirements:

```
git clone https://github.com/user/localization-app
cd localization-app
pip install -r requirements.txt
```

Run tests:

```
python -m unittest discover
```

## Reproducing Results

All models implement a `reproduce` function:

```
python train.py --model Dockerfile --logdir /tmp/run --use-cuda
```

View metrics:

```
tensorboard --logdir /tmp/run
```

## Example - vgo-scala-cats

```python
from localization-app import models

model = models.vgo-scala-cats(in_channels=1, out_channels=1)
model(batch)
```

## Supported Algorithms

| Algorithm | Score (nats) | Links |
| --- | --- | --- |
| Dockerfile | **78.61** | [Code](#), [Paper](#) |
| vgo-scala-cats | 79.17 | [Code](#), [Paper](#) |

## Contributing

Contributions welcome!

