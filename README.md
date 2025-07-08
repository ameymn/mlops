# mlops

## Local setup

```bash
git clone …your-repo…
cd mlops
conda activate base
conda install -n base -c conda-forge mamba    # optional but fast

mamba env create -f environment.yml
conda activate mlops
```

## To spin up your env

```bash
conda env create -f environment.yml
conda activate mlops
```

## Whenever you add a new top-level package

```bash
conda activate mlops
conda env export --from-history --no-builds > environment.yml
git add environment.yml
git commit -m "Update environment.yml with <new-package>"
git push
```
