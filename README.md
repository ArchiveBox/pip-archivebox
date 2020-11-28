# pip-archivebox

The official `pip` package for [ArchiveBox](https://github.com/ArchiveBox/ArchiveBox), the self-hosted internet archiving solution.

https://pypi.org/project/archivebox/

## Quickstart

**Install it:**
```bash
pip install --upgrade archivebox
```

**Try it out:**
```bash
archivebox version

mkdir data && cd data
archivebox init
archivebox add 'https://example.com'
```
---

Tested on macOS 10.15 and Ubuntu 20.04, should work on most systems (including Linux, BSD, macOS, and Windows).

---

## Development

The Pip package is built using [`setuptools`](https://setuptools.readthedocs.io/en/latest/) and hosted on PyPI.

https://pypi.org/project/archivebox/

The config file / package definition is here: [`ArchiveBox/setup.py`](https://github.com/ArchiveBox/ArchiveBox/blob/master/setup.py).

To build this package, make sure you are in the ArchiveBox main repo first.

```bash
cd ArchiveBox/
git pull --recurse-submodules

# Build the debian package
./bin/build_pip.sh

# Install it locally for testing
pip install -e .

# Release the debian package to the LaunchPad PPA
./bin/release.sh
```
