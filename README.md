# legos.codinglove

_A Legobot plugin_

[![Travis](https://img.shields.io/travis/Legobot/legos.codinglove.svg)]() [![PyPI](https://img.shields.io/pypi/pyversions/legos.codinglove.svg)]() [![PyPI](https://img.shields.io/pypi/v/legos.codinglove.svg)]()

[![PyPI](https://img.shields.io/pypi/wheel/legos.codinglove.svg)]() [![PyPI](https://img.shields.io/pypi/l/legos.codinglove.svg)]() [![PyPI](https://img.shields.io/pypi/status/legos.codinglove.svg)]()

## Usage

This lego listens for `!codinglove` at the beginning of a message and returns a random post from [The Coding Love](http://thecodinglove.com/)

## Installation

## Installation
`pip3 install legos.wtf`

This is a Lego designed for use with [Legobot](https://github.com/Legobot/Legobot), so you'll get Legobot along with this. To deploy it, import the package and add it to the active legos like so:

```python
# This is the legobot stuff
from Legobot import Lego
# This is your lego
from legos.codinglove import CodingLove
# This is a connector
from Legobot.Connectors.Slack import Slack

# Legobot stuff here
lock = threading.Lock()
baseplate = Lego.start(None, lock)
baseplate_proxy = baseplate.proxy()

# Add your lego
baseplate_proxy.add_child(CodingLove)

# Add a connector so you can send messages to it
baseplate_proxy.add_child(Slack, token='xoxb-aaaa-bbbb-ccccc')
```

## Tweaking

While you can use this one as-is, you could also add a localized version to your Legobot deployment by grabbing [codinglove.py](legos/codinglove.py) and deploying is as a local module. [Example of a Legobot instance with local modules](https://github.com/voxpupuli/thevoxfox/)

## Contributing

As always, pull requests are welcome.
