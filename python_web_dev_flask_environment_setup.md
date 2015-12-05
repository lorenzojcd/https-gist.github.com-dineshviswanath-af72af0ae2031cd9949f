
#Starting Python Web development in Mac OS X#

**Objective:** Getting started with Python Development
**Operating System:** Mac OS X
**Python version installed:** 3.5 (5th December 2015)


Downoad the lastest Python from https://www.python.org/downloads/

Mac OS uses default 2.x version out of box.
To check whether, python has been installed successfully. try the following command.

    python3 -V
    Python 3.5.0

Above step ensure that Python 3.5 has been installed successfully.

This is the high level outline of this post:
Mas OS X -> Python 3.5 -> Virtaulenv -> Flask --> app.py(first Hello world )


Installing virtaulenv: (Step 1 of 
Why use virtualenv?
1. Having different version of libraries for different projects
2. Solves the elevated privillege issue as virtualenv allows you to install with user permission

    sudo pip3 install virtualenv
    virtualenv --version
    13.1.2

Now lets create the first flask app
    mkdir ~/project
    cd ~/projets

Now we will create a virtualenv
    virtualenv hello_flask
    cd hello_flask

If you list the contents of the hello_flask directory, you will see that it has created several sub-directories, including a bin folder (Scripts on Windows) that contains copies of both Python and pip. The next step is to activate your new virtualenv.
        source bin/activate

Installing Flask in your virtaulenv

    pip install Flask

Hello, Flask

Create a new file called app.py
```python
		from flask import Flask
		
		app = Flask(__name__)
		
		@app.route('/')
		def index():
		    return 'Hello, Flask!'
		
		if __name__ == '__main__':
		    app.run(debug=True)

````
Open the web browser with ```http://localhost:5000```


    





