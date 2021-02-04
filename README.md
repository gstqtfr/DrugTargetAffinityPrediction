# Drug-target binding affinity prediction: based on DeepDTA

The approach used in this work is the modeling of protein sequences and compound 1D representations (SMILES) with convolutional neural networks (CNNs) to predict the binding affinity value of drug-target pairs.

This is an update of the DeepDTA code; please see the [readme](https://github.com/hkmztrk/DeepDTA/blob/master/data/README.md) for the source material.

## Requirements

These have been updated from the original code base. Working on the (currently!) contemporary versions of:

*  [Python 3.8.5 <=](https://www.python.org/downloads/)
*  [Keras 2.4.3](https://pypi.org/project/Keras/)
*  [Tensorflow 2.2.0](https://www.tensorflow.org/install/)
*  numpy
*  matplotlib

You have to place the "data" folder under the "source" directory. 

# Usage
```
python run_experiments.py --num_windows 32 \
                          --seq_window_lengths 8 12 \
                          --smi_window_lengths 4 8 \
                          --batch_size 256 \
                          --num_epoch 100 \
                          --max_seq_len 1000 \
                          --max_smi_len 100 \
                          --dataset_path 'data/kiba/' \
                          --problem_type 1 \
                          --log_dir 'logs/'


```

As explained above, this is an updating of the code; the original paper can be found here:


**For citation:**

```
@article{ozturk2018deepdta,
  title={DeepDTA: deep drug--target binding affinity prediction},
  author={{\"O}zt{\"u}rk, Hakime and {\"O}zg{\"u}r, Arzucan and Ozkirimli, Elif},
  journal={Bioinformatics},
  volume={34},
  number={17},
  pages={i821--i829},
  year={2018},
  publisher={Oxford University Press}
}
```
