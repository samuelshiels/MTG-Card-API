# MTG-Card-API

```python
# Use the Scryfall module
from mtg_card_api import ScryfallAPI

api = ScryfallAPI()
res = api.get_card_by_name("Sacred Foundry")

# Check if response encountered an error
if res.error is False:
    # Otherwise response prop will contain result string
    print(res.response) 
# {"object":"card","id":"8076a8c3-7c6c-4636-b5d8-9b09ee95f92c","oracle_id":"45181cb8-2090-4471-ba90-e5a8f04d525f","multiverse_ids":[643292],"mtgo_id":121137,"tcgplayer_id":517644,"cardmarket_id":748638,"name":"Sacred Foundry"...,"cardhoarder":"https://www.cardhoarder.com/cards/121137?affiliate_id=scryfall&ref=card-profile&utm_campaign=affiliate&utm_medium=card&utm_source=scryfall"}}
```

Default values for module will cache the result for 24hrs in `$XDG_HOME/.cache/MTGScryfallAPI` using `diskcache`

# Requirements 
  - rest_client_micro
  - diskcache

# Installation

```bash
pip install mtg_card_api
```