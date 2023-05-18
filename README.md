# Shoot the Fruits
This is a simple web game. The goal is to shoot as many fruits as possible.

 Written in Flask 2.3.2

<img src="https://github.com/xaoccc/Fruits-Web-Game/blob/main/static/explosion.png?raw=true" width=100% />

Basic moments in creating a small Flask app (with no DB):
1. Select/install virtual environment. It can be done either via settings->Project: [project name] > Project Interpreter section or command in the terminal. More about the terminal command <a href="https://stackoverflow.com/questions/22288569/how-do-i-activate-a-virtualenv-inside-pycharms-terminal">Here<a/>  
2. Install Flask. In PyCharm terminal write pip install Flask.  
3. Create necessary files/folders: in the priject dir create:  
 * Folder named "templates" for all html files. There should be at least 1 html file.  
 * Folder named "static" for all css, png and other media files.  
 * File named with the name of the app, for example app_name.py.  
4. Inside app_name.py import Flask, render_template, redirect, request  
5. After the import, write app = Flask(\_\_name\_\_). \_\_name\_\_ is used to find all static assets, templates and so on.  
6. Create routes. render_template will render each html file and all variables used in app_name.py, so you should have something like this: 
 
 ```@app_name.route('/') <- '/' for main domain 127.0.0.1:5000, '/subdomain' for subdomain 127.0.0.1:5000/subdomain  
 def index():  
    return render_template("index.html", var1-var1, var2=var2...) <- here we render files from temlates folder and variables from app_name.py
 ``` 
 7. Start the server. Usually we do it like this.  
 ```
 if __name__ == "__main__":  
     app.run()
 ```  
 8. Start and stop the server after every change, so you can see if it works as supposed to. 
 9. Turn debug on. When you run the app in the terminal using the command 
 ```
 flask run 
 ```
 In the directory of your app and in your virtual environment. If you see an error "500 Internal Server Error", look in the terminal and find the row in your code, where the mistake is and fix it.
 Then try again and again until the app runs properly :)
 ```
 if __name__ == "__main__":
    app.run(debug=True)
 ```
 10. Double check each command, setting, route and variable. All is case sensitive and one small mistake may crash the whole app.  
 
 Enjoy :)
