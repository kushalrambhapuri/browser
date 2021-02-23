# browser
This is your own browser where you can do everything and anything you want and you can do the same things what you do in Google chrome or whatever browser you use in your own browser.
I have done it by using Pycharm which is an python code editor.
Functionalities are You can go Back, Forward, Reload the page, or go to the Home page there is a address bar too.
For the code I have used a pip (python installation package) which are **pip install PyQt5** and **pip install PyQtWebEngine**
I have installed the same both packages in the terminal.
Now in the first I have imported sys.
I have took PyQt5.QtCore, PyQt5.QtWidgets and PyQt5.QtWebEngineWidgets and I have imported them.
Then the class MainWindow(QMainWindow) this is the Main Window inside that I have put def __init__(self): here init means initiate and super(MainWindow, self).__init__()
and after that self.browser = QWebEngineView() and self.browser.setUrl(QUrl('http://google.com')) this is for the default which you want to see when your browser opens and after that we have put self.setCentralWidget(self.browser) in this code we are telling him to Put the browser widget in the middle and then we have put self.showMaximized() it means the browser will be in full screen.
Then we have made a variable named navbar and the value is QToolBar() and then we have put self.addToolBar(navbar) this means we are making a small toolbar type where we can put the Back Nutton, Forward Button, Reload Button, Home Button and the address bar.
Then we have made another variable called back_btn and entered the value as QAction('Back', self) and then we have said that is the back_btn is triggered do a connection which is in the self.browser go back in the same way we have done it to the forward button, reload button and the home button.
Then we come to the address bar for the address bar we have put it we have created a variable called self.url_bar and the value in it is QLineEdit() and then we have put self.url_bar.returPressed.connect(self.navigate_to_url) and then we have told navbar to add this widget.
And then to change the url in the address bar we have put a code which is self.browser.urlChanged.connect(self.update_url) this is the code for updating the url in the address bar.
And after that we have put def navigate_home(self): and inside that we will put self.browser.setUrl(QUrl('http://google.com')) and then we have put another def navigate_to_url(self): and then we have put another one which we have put def update_url(self, q): anf under it I have written self.url_bar.setText(q.toString()).
And then at last to run the browser I have written some small code which are: app = QApplication(sys.argv) and QApplication.setApplicationName ('**Here you should write what name should be displayed in your browser in the top left corner**') and then window = MainWindow() and to execute the app I have written app.exec_() here exec means execute.
Now you are ready to run the browser now you can ditch the browser and use your own made browser!!!
