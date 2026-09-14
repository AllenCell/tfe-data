# Migration

## From v1 to v2

1. Update imports to reflect the new package name and repository location:

```
# pip
pip install git+https://github.com/AllenCell/tfe-data.git@v2.0.0

# requirements.txt
tfe_data @ git+https://github.com/AllenCell/tfe-data.git@v2.0.0
```

2. Rename the package in any imports from `colorizer_data` to `tfe_data`.

3. Replace renamed methods and classes. The old methods/classes will continue to
   work, but are marked as deprecated and will be removed in the next major
   version.
   - Replace `convert_colorizer_data()` with `convert_tfe_data()`.
   - Replace `ColorizerMetadata` with `DatasetMetadata`.
