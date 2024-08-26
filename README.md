# Parallel Transformers

Codebase for the paper [Towards Parallelising Pre-Trained Transformers](https://www.overleaf.com/read/zmctbmkqwbfc#4cc430).
In the paper we explore the effect of iterating through parallelised pre-trained transformer layers.
The paper was presented during the [DEARING 2024 workshop](https://dearing2024.di.uniba.it/landing).

## Repository structure

This repository is organised into four main directories:

```
|- experiments/
  |- ...
|- notebooks/
  |- ...
|- resources/
  |- configs/
    |- ...
  |- models/
    |- ...
|- submodules/
  |- ...
```

For further details, refer to the `README.md` within each directory.

## Environment setup

To install all the required packages within an Anaconda environment, run the following commands:

```bash
# Create anaconda environment 
conda create -n paratr python=3.12
# Activate anaconda environment
conda activate paratr
# Install required packages
conda install cuda -c nvidia
git submodule init; git submodule update
cd submodules/transformer_wrappers && pip install -r requirements.txt
git submodule init; git submodule update
cd submodules/lm-evaluation-harness && pip install -e .
```

To add the source code directory(ies) to the Python path, you can add this line to the file `~/.bashrc`

```bash
export PYTHONPATH=$PYTHONPATH:/path/to/parallel_tranformers/submodules/transformer_wrappers/src
```

To run the unit tests you will need to add the [Hugging-Face authentication token](https://huggingface.co/docs/hub/security-tokens) to your environment variables:

```bash
export HUGGING_FACE_TOKEN=...
```

## References

If you are willing to use our code or our models, please cite us with the following reference(s):

```bibtex
...
```


## Acknowledgements

- Vincenzo Scotti: ([vincenzo.scotti@polimi.it](mailto:vincenzo.scotti@polimi.it))
- Mark James Carman: ([mark.carman@polimi.it](mailto:mark.carman@.polimi.it))
