# Anki Setup

## Prerequisites (one-time)

1. **Anki Desktop** — install from the official Anki website.
2. **AnkiWeb account** — free, handles sync between desktop and phone.
3. **Anki mobile app** — available for iOS and Android.
4. **AnkiConnect add-on** — enables direct card injection via API. Install through Anki Desktop's add-on manager. Exposes a localhost:8765 API.

## Importing the cards

1. Open Anki Desktop.
2. File → Import → select the `.txt` file from `cards/`.
3. Note type: **Basic** (front / back / tags).
4. Assign to a deck, then import.
5. Sync to AnkiWeb, then sync on your phone.

## Adding cards via AnkiConnect

With AnkiConnect installed and Anki Desktop open, a coding agent can POST cards directly:

```python
import requests

def add_card(front, back, deck="ML-vocab", tags=None):
    note = {
        "deckName": deck,
        "modelName": "Basic",
        "fields": {"Front": front, "Back": back},
        "tags": tags or [],
        "options": {"allowDuplicate": False}
    }
    r = requests.post("http://localhost:8765", json={
        "action": "addNote",
        "version": 6,
        "params": {"note": note}
    })
    return r.json()
```

## Card files

| File | Deck | Topics |
|------|------|--------|
| cards/ml-vocab.txt | ML-vocab | ML fundamentals, SAE, metagenomics, ESM, scaling laws |
| cards/food-science.txt | food-science | Blooming, flavor stacking, emulsification, Maillard, Koji |

## Card design rules

See `pedagogy/scaffold.md` for the full reasoning. Short version:

- One fact per card
- Back: definition + concrete example
- Tags: `topic subtopic` (e.g., `ml-vocab sae`)
- Three cards per concept minimum: definition, application, connection
