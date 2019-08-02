# Proxy-Settings
Notes of proxy settings for conda, pip, python scripts.

---------------------

## Pip
Install or upgrade packages with `pip`:
```ruby
pip install package --proxy=http://your_proxy:your_port
```

## Conda
On Windows:
```ruby
set http_proxy=http://your_proxy:your_port
set https_proxy=https://your_proxy:your_port
conda install package
```

On Linux in `bash`:
```ruby
export http_proxy=http://your_proxy:your_port
export https_proxy=https://your_proxy:your_port
conda install package
```

## Python scripts
```ruby
import os

proxy = 'your_proxy:your_port'
os.environ['http_proxy'] = proxy
os.environ['HTTP_PROXY'] = proxy
os.environ['https_proxy'] = proxy
os.environ['HTTPS_PROXY'] = proxy

*your code*
```
