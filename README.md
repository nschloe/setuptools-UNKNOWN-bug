Reproducing the bug:

```
pip install .
```

Output:
```
Processing /path/to/setuptools-UNKNOWN-bug
  Installing build dependencies ... done
  Getting requirements to build wheel ... done
  Installing backend dependencies ... done
  Preparing metadata (pyproject.toml) ... done
Building wheels for collected packages: UNKNOWN
  Building wheel for UNKNOWN (pyproject.toml) ... done
  Created wheel for UNKNOWN: filename=UNKNOWN-0.0.0-py3-none-any.whl size=961 sha256=91c64bbb4a47b83367a740ca84e31ff027cd4c72b381fc0d0a1d4d03bf0a1030
  Stored in directory: /path/to/home/.cache/pip/wheels/8c/53/6f/b8f9907b9ed054106c802dcf084e59af6c78e96adc189caa9c
Successfully built UNKNOWN
Installing collected packages: UNKNOWN
  Attempting uninstall: UNKNOWN
    Found existing installation: UNKNOWN 0.0.0
    Uninstalling UNKNOWN-0.0.0:
      Successfully uninstalled UNKNOWN-0.0.0
Successfully installed UNKNOWN-0.0.0
```

It all works well with [build](https://github.com/pypa/build):
```
python3 -m build
```
```
* Creating virtualenv isolated environment...
* Installing packages in isolated environment... (setuptools>=61)
* Getting dependencies for sdist...
/tmp/build-env-6fxzctbf/lib/python3.10/site-packages/setuptools/config/pyprojecttoml.py:102: _ExperimentalProjectMetadata: Support for project metadata in `pyproject.toml` is still experimental and may be removed (or change) in future releases.
  warnings.warn(msg, _ExperimentalProjectMetadata)
running egg_info
writing src/foobar.egg-info/PKG-INFO
writing dependency_links to src/foobar.egg-info/dependency_links.txt
writing top-level names to src/foobar.egg-info/top_level.txt
reading manifest file 'src/foobar.egg-info/SOURCES.txt'
writing manifest file 'src/foobar.egg-info/SOURCES.txt'
* Building sdist...
/tmp/build-env-6fxzctbf/lib/python3.10/site-packages/setuptools/config/pyprojecttoml.py:102: _ExperimentalProjectMetadata: Support for project metadata in `pyproject.toml` is still experimental and may be removed (or change) in future releases.
  warnings.warn(msg, _ExperimentalProjectMetadata)
running sdist
running egg_info
writing src/foobar.egg-info/PKG-INFO
writing dependency_links to src/foobar.egg-info/dependency_links.txt
writing top-level names to src/foobar.egg-info/top_level.txt
reading manifest file 'src/foobar.egg-info/SOURCES.txt'
writing manifest file 'src/foobar.egg-info/SOURCES.txt'
running check
warning: check: missing required meta-data: url

warning: check: missing meta-data: either (author and author_email) or (maintainer and maintainer_email) should be supplied

creating foobar-1.2.3
creating foobar-1.2.3/src
creating foobar-1.2.3/src/foobar
creating foobar-1.2.3/src/foobar.egg-info
copying files to foobar-1.2.3...
copying README.md -> foobar-1.2.3
copying pyproject.toml -> foobar-1.2.3
copying src/foobar/__about__.py -> foobar-1.2.3/src/foobar
copying src/foobar/__init__.py -> foobar-1.2.3/src/foobar
copying src/foobar/_main.py -> foobar-1.2.3/src/foobar
copying src/foobar.egg-info/PKG-INFO -> foobar-1.2.3/src/foobar.egg-info
copying src/foobar.egg-info/SOURCES.txt -> foobar-1.2.3/src/foobar.egg-info
copying src/foobar.egg-info/dependency_links.txt -> foobar-1.2.3/src/foobar.egg-info
copying src/foobar.egg-info/top_level.txt -> foobar-1.2.3/src/foobar.egg-info
Writing foobar-1.2.3/setup.cfg
Creating tar archive
removing 'foobar-1.2.3' (and everything under it)
* Building wheel from sdist
* Creating virtualenv isolated environment...
* Installing packages in isolated environment... (setuptools>=61)
* Getting dependencies for wheel...
/tmp/build-env-l4_wond4/lib/python3.10/site-packages/setuptools/config/pyprojecttoml.py:102: _ExperimentalProjectMetadata: Support for project metadata in `pyproject.toml` is still experimental and may be removed (or change) in future releases.
  warnings.warn(msg, _ExperimentalProjectMetadata)
running egg_info
writing src/foobar.egg-info/PKG-INFO
writing dependency_links to src/foobar.egg-info/dependency_links.txt
writing top-level names to src/foobar.egg-info/top_level.txt
reading manifest file 'src/foobar.egg-info/SOURCES.txt'
writing manifest file 'src/foobar.egg-info/SOURCES.txt'
* Installing packages in isolated environment... (wheel)
vi* Building wheel...
/tmp/build-env-l4_wond4/lib/python3.10/site-packages/setuptools/config/pyprojecttoml.py:102: _ExperimentalProjectMetadata: Support for project metadata in `pyproject.toml` is still experimental and may be removed (or change) in future releases.
  warnings.warn(msg, _ExperimentalProjectMetadata)
running bdist_wheel
running build
running build_py
creating build
creating build/lib
creating build/lib/foobar
copying src/foobar/__about__.py -> build/lib/foobar
copying src/foobar/__init__.py -> build/lib/foobar
copying src/foobar/_main.py -> build/lib/foobar
running egg_info
writing src/foobar.egg-info/PKG-INFO
writing dependency_links to src/foobar.egg-info/dependency_links.txt
writing top-level names to src/foobar.egg-info/top_level.txt
reading manifest file 'src/foobar.egg-info/SOURCES.txt'
writing manifest file 'src/foobar.egg-info/SOURCES.txt'
installing to build/bdist.linux-x86_64/wheel
running install
running install_lib
creating build/bdist.linux-x86_64
creating build/bdist.linux-x86_64/wheel
creating build/bdist.linux-x86_64/wheel/foobar
copying build/lib/foobar/__about__.py -> build/bdist.linux-x86_64/wheel/foobar
copying build/lib/foobar/__init__.py -> build/bdist.linux-x86_64/wheel/foobar
copying build/lib/foobar/_main.py -> build/bdist.linux-x86_64/wheel/foobar
running install_egg_info
Copying src/foobar.egg-info to build/bdist.linux-x86_64/wheel/foobar-1.2.3-py3.10.egg-info
running install_scripts
creating build/bdist.linux-x86_64/wheel/foobar-1.2.3.dist-info/WHEEL
creating '/path/to/setuptools-UNKNOWN-bug/dist/tmpc0sd_oel/foobar-1.2.3-py3-none-any.whl' and adding 'build/bdist.linux-x86_64/wheel' to it
adding 'foobar/__about__.py'
adding 'foobar/__init__.py'
adding 'foobar/_main.py'
adding 'foobar-1.2.3.dist-info/METADATA'
adding 'foobar-1.2.3.dist-info/WHEEL'
adding 'foobar-1.2.3.dist-info/top_level.txt'
adding 'foobar-1.2.3.dist-info/RECORD'
removing build/bdist.linux-x86_64/wheel
Successfully built foobar-1.2.3.tar.gz and foobar-1.2.3-py3-none-any.whl
```
