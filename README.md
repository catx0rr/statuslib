# statuslib
Status Indicators on print statements for your python script.

---

# Usage:
import statuslib
from statuslib import status


## Static methods for status Class

- status.log(string, code=code, color=color, text=bool, logging=bool)
- status.info(string, text=bool, logging=bool)
- status.success(string, text=bool, logging=bool)
- status.failed(string, text=bool, logging=bool)
- status.working(string, text=bool, logging=bool)
- status.warning(string, text=bool, logging=bool)

## Arguments

Default string code arguments:
- info
- success
- failed
- working
- warning

### Imprinter Class

Additional arguments that can be used graphically:
- shell
- root
- prompt

Methods:
- custom_imprint and custom_code method 
    - ```x = Imprinter(string, code=code, text=bool, customize=string logging=bool)```
    - ```x.custom_imprint()```
    - ```x.custom_code()```

- imprint method
    - ``` x = Imprinter(string, code=code, text=bool, logging=bool)```
    - ```x.imprint()```

- raw_imprint method
    - ``` x = Imprinter(string, code=code, text=bool, logging=bool)```
    - ```returns tuple of the output```

### Colorizer Class

Available colors:
- <span style="color:#00FFFF">cyan</span>
- <span style="color:#008000">green</span>
- <span style="color:#ff0000">red</span>
- <span style="color:#800080">purple</span>
- <span style="color:#FFFF00">yellow</span>
- <span style="color:#0000FF">blue</span>
- <span style="color:#808080">gray</span>
- <span style="color:#000000">white</span>

Bold colors:
- <span style="color:#00FFFF">b_cyan</span>
- <span style="color:#008000">b_green</span>
- <span style="color:#ff0000">b_red</span>
- <span style="color:#800080">b_purple</span>
- <span style="color:#FFFF00">b_yellow</span>
- <span style="color:#0000FF">b_blue</span>
- <span style="color:#808080">b_gray</span>
- <span style="color:#000000">b_white</span>

Custom colors:
- ```c=0; for i in {0..255}; do if [ $c == 12 ]; then echo; c=0; else printf "\x1b[38;5;${i}mcolor${i}\033[00m"; ((c++)); fi; done```

---
Custom color pallete

![color pallete](https://github.com/catx0rr/statuslib/blob/master/img/colors.PNG)
---


Methods:
- colorize method
    - ``` x = Colorizer(string, color=color)```
    - ``` x.colorize()```

---

# Sample Image

![status messages](https://github.com/catx0rr/statuslib/blob/master/img/sample.PNG)

---

![terminal test](https://github.com/catx0rr/statuslib/blob/master/img/terminal.PNG)

---

![complete logging](https://github.com/catx0rr/statuslib/blob/master/img/complete_logging.PNG)

---

# Known Issues

- Does not support windows cmd and ps shells yet for text colorization. 
- Works perfectly on Bash shells (Mac / Linux)

---

# Licensing

Licensed under [GNU General Public License v3.0](https://github.com/catx0rr/statuslib/blob/master/LICENSE)

© Copyright War Torrente
