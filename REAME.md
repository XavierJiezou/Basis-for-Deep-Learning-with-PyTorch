# Basis-for-Deep-Learning-with-PyTorch

## Documentation

### Sphinx

- Install

```bash
git clone https://github.com/XavierJiezou/Basis-for-Deep-Learning-with-PyTorch.git
cd Basis-for-Deep-Learning-with-PyTorch/
pip install -r docs/requirements.txt
cd docs/
```

- Build

```bash
make html
```

- Deploy

```bash
sphinx-autobuild source build/html
```

### MkDocs

- Install

```bash
git clone https://github.com/XavierJiezou/Basis-for-Deep-Learning-with-PyTorch.git
cd Basis-for-Deep-Learning-with-PyTorch/
pip install -r docs/requirements.txt
cd docs/
```

- Build

```bash
mkdocs build -f mkdocs.yml
```

- Deploy

```bash
mkdocs serve -f mkdocs.yml
```

