Reproducing the bug:

```
python3 -m build --sdist
```

```
ModuleNotFoundError: No module named 'rich'
```

Change the import order in `__init__.py` such that `__about__` comes first, and
it will succeed.
