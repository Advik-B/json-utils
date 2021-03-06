# Converting `dict` object to Json and writing it to a file

```py

from json_util import *

fruits = ['apple',
          'banana',
          'cherry',
          'mango',
          'watermelon',
          'cranberry',
          'avacado',
          'tomato',
          # The list goes on ...
          ]

veggies = ['lemon',
           'beans',
           'bottle guard',
           'spinach',
           'chilli',
           'brinjal', # (EggPlant)
            # The list goes on
           ]

fruits_n_veggies = { # This is a `dict` type

    'Fruits':fruits,
    'Veggies':veggies,
    }

fruits_n_veggies_json = convert_json(data=fruits_n_veggies, mode=json_modes().DICT_TO_JSON)

write_json(Json_Data=fruits_n_veggies_json, file_name='Fruits & Veggies.json', overwrite=True, indent_size=4)
# The mode indentation the better it looks
```
The result:

```json
{
    "Fruits": [
        "apple",
        "banana",
        "cherry",
        "mango",
        "watermelon",
        "cranberry",
        "avacado",
        "tomato"
    ],
    "Veggies": [
        "lemon",
        "beans",
        "bottle guard",
        "spinach",
        "chilli",
        "brinjal"
    ]
}
```
