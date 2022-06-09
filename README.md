# pyfieldlib
pyfieldlib library is used to define fields in a simple way.  
## Install
`pip install pyfieldlib`  
## Documentation
[pyfieldlib wiki](https://github.com/DuelitDev/pyfieldlib/wiki)  
## Example
```python
from pyfieldlib import *


class Human(metaclass=FieldMeta):
    _age = 19
    
    @fields
    def age(self):
        return Human._age

    @age.setter
    def age(self, value):
        Human._age = value


# get
print(Human.age)  # 19

# set
Human.age = 20
print(Human.age)  # 20
```   
## Copyright
Copyright 2022. Kim Jae-yun all rights reserved.  
## License
[MIT License](https://github.com/DuelitDev/pyfieldlib/blob/main/LICENSE)   

