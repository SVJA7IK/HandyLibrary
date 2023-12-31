# HandyLibrary
[![Python 3.10](https://img.shields.io/badge/python-3.10-blue.svg)](https://www.python.org/downloads/release/python-31013/)

A library that makes it very convenient to perform standard actions in Python
## Installation
### Using PyPI
The latest stable release is available on PyPI, and you can install it by saying
```
python -m pip install handy-library 
```

## Example
Example of configuring automatic creation of `config.json`
```
from handylib.tools import ConfigLoader

cl = ConfigLoader()
cl.load_config("config.json", [cl.ConfigParam('test', value=[1, 2, 3], description="Params", value_type=list)])
```
The `config.json` file that resulted from the output
```
{
    "test_1_description": "Params",
    "test_1": [1, 2, 3],
    "test_2": 0.123,
    "test_3": true
}
```