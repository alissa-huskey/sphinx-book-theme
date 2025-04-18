
# Add a download page button

You can add a button allowing users to download the currently viewed page in several formats: `raw source`, `pdf` or `ipynb` if one was generated as part of the build.
To include this button, use the following configuration:

`````{tab-set}

````{tab-item} conf.py
:sync: conf.py

```python
html_theme_options = {
    ...
    "use_download_button": True,
    ...
}
```

````

````{tab-item} _config.yml
:sync: _config.yml

```yaml
sphinx:
    config:
        html_theme_options:
            use_download_button: true
```

````

`````


```{note}
This theme over-rides the Sphinx default for `html_sourcelink_suffix` to be `''` instead of `.txt`.
This is because most users of this theme want to download source files of the pages themselves, which do not begin with `.txt`.
If you wish to add a different source suffix, manually specify `html_sourcelink_suffix` in `conf.py`.
```
