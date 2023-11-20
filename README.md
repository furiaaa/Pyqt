from PyQt5.QtWidgets import *
import sys


class MainWindow(QMainWindow): # главное окно
    def __init__(self, parent=None):
        super().__init__(parent)
        self.setupUi()
    def setupUi(self):
        self.setWindowTitle("Hello, world") # заголовок окна
        self.move(300, 300) # положение окна
        self.resize(200, 200) # размер окна
        self.lbl = QLabel('<i>Hello</i>, <b>world</b>!!!', self)
        self.lbl.move(30, 30)
        self.lbl2 = QLabel('<u>Ещё одна метка</u>', self)
        self.lbl2.move(50, 50)


if __name__ == "__main__":
    app = QApplication(sys.argv)
    win = MainWindow()
    win.show()
    sys.exit(app.exec_())
