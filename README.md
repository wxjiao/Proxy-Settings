# Proxy-Settings
Notes of proxy settings for conda, pip, python scripts.

---------------------

## Conda
On Windows in `cmd`:
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

## Pip
For Pip, you can set up the global proxy as Conda above.

Or you can designate the proxy argument in `pip` as:
```ruby
pip install package --proxy=http://your_proxy:your_port
```

## Python scripts
For Python, you can also set up the global proxy as Conda above.

Or just set up in your python scripts as:
```ruby
import os

proxy = 'your_proxy:your_port'
os.environ['http_proxy'] = proxy
os.environ['HTTP_PROXY'] = proxy
os.environ['https_proxy'] = proxy
os.environ['HTTPS_PROXY'] = proxy

# your code
```
