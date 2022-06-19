# Basis-for-Deep-Learning-with-PyTorch

## Examples

> [https://github.com/aianaconda/pytorch-GNN-1st](https://github.com/aianaconda/pytorch-GNN-1st)

## Documentation

### MkDocs

- Install

```bash
git clone https://github.com/XavierJiezou/Basis-for-Deep-Learning-with-PyTorch.git
cd Basis-for-Deep-Learning-with-PyTorch/docs/
pip install -r requirements.txt
```

- Build

```bash
mkdocs build -f mkdocs.yml
```

- Deploy

```bash
mkdocs serve -f mkdocs.yml
```

### Sphinx

- Install

```bash
git clone https://github.com/XavierJiezou/Basis-for-Deep-Learning-with-PyTorch.git
cd Basis-for-Deep-Learning-with-PyTorch/docs/
pip install -r requirements.txt
```

- Build

```bash
make html
```

- Deploy

```bash
sphinx-autobuild source build/html
```
