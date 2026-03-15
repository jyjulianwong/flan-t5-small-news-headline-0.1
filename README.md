# flan-t5-small-news-headline-0.1

## Get started with development

1. Clone the repository.

```bash
git clone https://github.com/jyjulianwong/flan-t5-small-news-headline-0.1.git
```

2. Verify that you have a compatible Python version installed on your machine.
```bash
python --version
```

3. Install [uv](https://github.com/astral-sh/uv) (used as the package manager for this project).

4. Install the development dependencies.
```bash
cd flan-t5-small-news-headline-0.1/
uv sync --all-groups
uv run pre-commit install
```

## Get started with Jupyter notebooks

1. Once the above setup is complete, set up a Python kernel.
```bash
source .venv/bin/activate
python -m ipykernel install --user --name=flan-t5-small-news-headline-0.1
```

2. Refer to the following common commands.
```bash
jupyter kernelspec list
jupyter kernelspec uninstall flan-t5-small-news-headline-0.1
```

3. Start the Jupyter server.
```bash
jupyter lab
```

## FAQs

### `datasets` package version restrictions

- `datasets==2.x.x`:
    - cannot handle Windows file path formats when determining path from cache and will mix with Linux file path formats
- `datasets==3.x.x`:
    - will "forget" global variables when running `.map(...)` due to `multiprocessing` module error
- `datasets==4.7.0`:
    - cannot handle dataset builder scripts (e.g. `financial-phrasebook`)
    - will "forget" global variables when running `.map(...)` due to `multiprocessing` module error