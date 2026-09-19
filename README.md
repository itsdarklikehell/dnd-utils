# dnd-utils

Utility library for D&D 5e game tools and character management.

## Installation

```bash
pip install dnd-utils
```

## Usage

```python
from dnd_utils import Character, Dice

# Roll dice
dice = Dice()
result = dice.roll("2d20+5")

# Create a character
char = Character(name="Gandalf", level=10, class_="Wizard")
```

## Development

```bash
pip install -e ".[dev]"
pytest
```

## License

MIT
