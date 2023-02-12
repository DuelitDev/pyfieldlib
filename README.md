# pyfieldlib
pyfieldlib library is used to define fields in a simple way.  
## Install
`pip install pyfieldlib`  
## Examples
```python
from pyfieldlib import *


class Human(metaclass=FieldMeta):
    _age = 19
    
    @fields
    def is_mammal(self):
        return True
    
    @fields
    def age(self):
        return Human._age

    @age.setter
    def age(self, value):
        Human._age = value


# get
print(Human.age)  # 19
print(Human.is_mammal)  # True

# set
Human.age = 20
print(Human.age)  # 20
Human.is_mammal = False  # Error
```   
## Copyright
Copyright 2023. DuelitDev all rights reserved.  
## License
[MIT License](https://github.com/DuelitDev/pyfieldlib/blob/main/LICENSE)   

