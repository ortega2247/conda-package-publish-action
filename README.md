# Publish Anaconda Package
A Github Action to publish your Python package to Anaconda repository.

### Example workflow
```yaml
name: Publish

on: [release]

jobs:
  publish:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - name: publish-to-conda
      uses: ortega2247/conda-package-publish-action@master
      with:
        subDir: '.'
        AnacondaToken: ${{ secrets.ANACONDA_TOKEN }}
```
