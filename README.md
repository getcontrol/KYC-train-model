# Train Tensorflow Model for Tensorflow Verification

This repo contains the Python code to produce the dataset and train the Tensorflow model for use in [KYC-tensorflow](https://github.com/getcontrol/KYC-tensorflow). This training model transfers learning from a previously trained model mobilenet_v2.

# Installation Instructions

1. Clone the repo.

``` git clone https://github.com/getcontrol/KYC-train-model ```

``` cd KYC-train-model```

2. Download and unzip the the MIDV-500 formatted dataset to 'verification-train-model' directory.

https://www.dropbox.com/s/dmjbat0e1re5rkf/midv_500.zip?dl=0

3. Make a 'data' directory in verification-train-model for the dataset generation and an 'output' folder for testing.

```mkdir data```

```mkdir output```

4. Create and activate a Python 3 Virtual environment.

```python3 -m venv env```

```source env/bin/activate```

5. Install Requirements.

```pip install -r requirements.txt```

6. Synthesize training data.

```python synthesis_data.py```

```python receipt_dataset.py```

7. Train model.

```python train.py```

# Test Model

Samples are included in 'test_samples_600*800'.

```python test.py```



### Citation
Please cite this paper, if using midv dataset, link for dataset provided in paper

    @article{DBLP:journals/corr/abs-1807-05786,
      author    = {Vladimir V. Arlazarov and
                   Konstantin Bulatov and
                   Timofey S. Chernov and
                   Vladimir L. Arlazarov},
      title     = {{MIDV-500:} {A} Dataset for Identity Documents Analysis and Recognition
                   on Mobile Devices in Video Stream},
      journal   = {CoRR},
      volume    = {abs/1807.05786},
      year      = {2018},
      url       = {http://arxiv.org/abs/1807.05786},
      archivePrefix = {arXiv},
      eprint    = {1807.05786},
      timestamp = {Mon, 13 Aug 2018 16:46:35 +0200},
      biburl    = {https://dblp.org/rec/bib/journals/corr/abs-1807-05786},
      bibsource = {dblp computer science bibliography, https://dblp.org}
    }
