# Pyside6 (Qt for python)

## ENV

### Installing

**Pyside6** require :

- Python **3.7+**
**Install** :

```shell
pip install pyside6
```

and import it in your _project_ .

### Folder tree

- Basic **file tree _preview_**:

```text
ParentFolder :
│   main.py
│   ui_wid.py
│
└───__pycache__ : "generated automatically by Pyside"
      ui_wid.cpython-312.pyc
```

### Files content

In the main program `"main.py"` by DEFUALT should have this code block :

```python
import sys
from PySide6.QtWidgets import QApplication
# import ui elements from separate file
from ui_wid import MainWindow
# write Logic here :


if __name__ == "__main__":
    app = QApplication(sys.argv)
    widget = MainWindow()
    widget.show()
    # start event Loop ---
    sys.exit(app.exec())
```

`"main.py"` imports "MainWindow()" class from `"ui_wid.py"` which contains this code :

```python
from PySide6.QtWidgets import QMainWindow, QLabel

class MainWindow(QMainWindow):
    def __init__(self) -> None:
        super().__init__()
        self.setWindowTitle("MainGui")
        myLabel = QLabel("Test Text Gui")
        self.setCentralWidget(myLabel)
```

and now if you run this code will pop up a window with a text inside .
