# Ancient-Chinese-Poem-Generator
This generator generates Chinese poem automatically when given the first sentence or the initial characters.
Two LSTMs are stacked together and trained as a generative model.

This is a group project for CSCI 544, Applied Natural Language Processing.

Members:
- Shengyu Chen
- Shuai Zhou
- Yizhao He
- Zichen Yang

# Requirements

- numpy, scipy
- yaml
- HDF5 and h5py
- TensorFlow
- Keras

# Usage

### Train
```sh
python ./lstm/train.py [-m SAVE_PATH] [-d DATA_PATH]
```

### Generate
```sh
python ./lstm/generate.py [-p PRIME] [-s SENTENCE] [-v VOCAB_PATH] [-w MODEL_WEIGHTS_PATH] [-m MODEL_STRUCT_PATH]
```

# Sample

	春至花海棠
	别来此归依
	风共旧知重
	山巢寥须难

# Parameters
The first version is a sequence to word language model based on LSTM programmed in Python with Keras.

- memory units number: 256 & 512
- dropout: 0.2
- batch size: 64
- epoch: 100+
- sequence length: 6 or 8

# Data Source
All poetry data comes from [JackyGao's work](https://github.com/jackeyGao/chinese-poetry), which is a great contribution for this model. Peotries are labed with special rhymes which are the rules Chinese poems need to follow. 

# License
MIT