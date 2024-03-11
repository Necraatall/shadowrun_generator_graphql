# TODO: install Taskfile
# TODO: install hatch
# TODO: install graphana do Taskfile
https://grafana.com/docs/grafana/latest/setup-grafana/installation/debian/

# TODO: spusteni
uvicorn app.main:app --reload
http://127.0.0.1:8000/graphql

# TODO: navrh nove adres struktury:
```
.
├── common
│   ├── database.py  # SQLite database
│   ├── schema.py  # GraphQL schema
│   ├── models
│   │   ├── __init__.py
│   │   ├── character.py
│   │   ├── name.py
│   │   ├── attribute.py
│   │   └── background.py
├── main.py
├── character
│   ├── __init__.py
├── name_generator
│   ├── __init__.py
├── attribute_generator
│   ├── __init__.py
├── background_generator
    ├── __init__.py
```

reseni models:
```
# Soubor: models/__init__.py

from .character import Character
from .name import Name
from .attribute import Attribute
from .background import Background
```

main.py
```
# Soubor: main.py

from common.models import Character, Name, Attribute, Background
```