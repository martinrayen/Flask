=========================================================================================================================================================
Virtual Environment : Setup and working
=========================================================================================================================================================
1. Install virtualenv package. 
	==> pip install virtualenv
2. Create a folder for setting-up virtual environment.
3. Create a virtual environment.
	==> C:\Users\HP\DevEnv\Projects\VirtualEnvironment>virtualenv Test
4. Activate the virtual environment.
	==> C:\Users\HP\DevEnv\Projects\VirtualEnvironment>"C:\Users\HP\DevEnv\Projects\VirtualEnvironment\Test\Scripts\activate.bat"
5. Launch the python interpreter within the virtual environment.
	==> (Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment>python
		   Python 3.7.3 (default, Mar 27 2019, 17:13:21) [MSC v.1915 64 bit (AMD64)] :: Anaconda, Inc. on win32
	>>> import numpy
	Traceback (most recent call last):
	  File "<stdin>", line 1, in <module>
	  ModuleNotFoundError: No module named 'numpy'
	>>> import sys
	>>> exit()		
6. Install the relevant modules required.
	==> (Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment>pip install numpy
	==> (Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment>pip install pandas

7. Execute a custom based python file.
	==> (Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment>python "C:\Users\HP\DevEnv\Projects\Test\Test.py"
	    Hello world	
8. Deactivate the virtual environment.
	==> (Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment>deactivate
	==> C:\Users\HP\DevEnv\Projects\VirtualEnvironment>

=========================================================================================================================================================
Flask : Lesson-1 Setup and development
=========================================================================================================================================================
01. Navigate/Activate to your virtual environment Test.
	==> C:\Users\HP\DevEnv\Projects\VirtualEnvironment>"C:\Users\HP\DevEnv\Projects\VirtualEnvironment\Test\Scripts\activate.bat"
	(Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment>
02. Install flask in this environment.
	==> (Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment>pip install flask
	Collecting flask
	  Downloading https://files.pythonhosted.org/packages/9b/93/628509b8d5dc749656a9641f4caf13540e2cdec85276964ff8f43bbb1d3b/Flask-1.1.1-py2.py3-none-	any.whl (94kB)
	     |████████████████████████████████| 102kB 2.2MB/s
	Collecting Jinja2>=2.10.1 (from flask)
	  Downloading https://files.pythonhosted.org/packages/1d/e7/fd8b501e7a6dfe492a433deb7b9d833d39ca74916fa8bc63dd1a4947a671/Jinja2-2.10.1-py2.py3-	none-any.whl (124kB)
	     |████████████████████████████████| 133kB 3.3MB/s
	Collecting click>=5.1 (from flask)
	  Downloading https://files.pythonhosted.org/packages/fa/37/45185cb5abbc30d7257104c434fe0b07e5a195a6847506c074527aa599ec/Click-7.0-py2.py3-none-	any.whl (81kB)
	     |████████████████████████████████| 81kB 5.1MB/s
	Collecting Werkzeug>=0.15 (from flask)
	  Downloading https://files.pythonhosted.org/packages/b7/61/c0a1adf9ad80db012ed7191af98fa05faa95fa09eceb71bb6fa8b66e6a43/Werkzeug-0.15.6-py2.py3-	none-any.whl (328kB)
	     |████████████████████████████████| 337kB 6.8MB/s
	Collecting itsdangerous>=0.24 (from flask)
	  Downloading https://files.pythonhosted.org/packages/76/ae/44b03b253d6fade317f32c24d100b3b35c2239807046a4c953c7b89fa49e/itsdangerous-1.1.0-py2.py3	-none-any.whl
	Collecting MarkupSafe>=0.23 (from Jinja2>=2.10.1->flask)
	  Downloading https://files.pythonhosted.org/packages/65/c6/2399700d236d1dd681af8aebff1725558cddfd6e43d7a5184a675f4711f5/MarkupSafe-1.1.1-cp37-	cp37m-win_amd64.whl
	Installing collected packages: MarkupSafe, Jinja2, click, Werkzeug, itsdangerous, flask
	Successfully installed Jinja2-2.10.1 MarkupSafe-1.1.1 Werkzeug-0.15.6 click-7.0 flask-1.1.1 itsdangerous-1.1.0

	==> (Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment>
03. Check, if flask installed correctly.
	(Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment>python
	Python 3.7.3 (default, Mar 27 2019, 17:13:21) [MSC v.1915 64 bit (AMD64)] :: Anaconda, Inc. on win32

	Warning:
	This Python interpreter is in a conda environment, but the environment has
	not been activated.  Libraries may fail to load.  To activate this environment
	please see https://conda.io/activation

	Type "help", "copyright", "credits" or "license" for more information.
	>>> import flask
	>>>
	>>> exit()

	(Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment>
04. Create a project folder Flask_Blog under the virtual environment.
	(Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment>mkdir Flask_Blog
05. Create flaskblog.py file that displays "Hello World"
06. Navigate to the directory Flask_Blog
	(Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment>cd Flask_Blog
	(Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment\Flask_Blog>	
07. Set the environment variable.
	(Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment\Flask_Blog>set FLASK_APP=flaskblog.py
	(Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment\Flask_Blog>
08. Run the flask server.
	(Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment\Flask_Blog>flask run
 	* Serving Flask app "flaskblog.py "
 	* Environment: production
   		WARNING: This is a development server. Do not use it in a production deployment.
   		Use a production WSGI server instead.
 	* Debug mode: off
 	* Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
09. Copy and paste the above URL to render the web page.
    Check the URL : http://localhost:5000 
    The file flaskblog.py has method Hello() decorated with route(\) home to display "Home" page.
10. Set the debug mode to True to enable changes to html and render without the need to restart web server.
	(Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment\Flask_Blog>set FLASK_DEBUG=1
	(Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment\Flask_Blog>
11. Run the flask server in debug mode.
	(Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment\Flask_Blog>flask run
 	* Serving Flask app "flaskblog.py " (lazy loading)
 	* Environment: production
   	WARNING: This is a development server. Do not use it in a production deployment.
   	Use a production WSGI server instead.
 	* Debug mode: on
 	* Restarting with stat
 	* Debugger is active!
 	* Debugger PIN: 950-169-851
 	* Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
12. Stop the flask server and have the python script start the server.
	Press ctrl + C
	(Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment\Flask_Blog>
13. Call the custom python file to start the server.
	(Test) C:\Users\HP\DevEnv\Projects\VirtualEnvironment\Flask_Blog>python flaskblog.py
 	* Serving Flask app "flaskblog" (lazy loading)
 	* Environment: production
   	WARNING: This is a development server. Do not use it in a production deployment.
   	Use a production WSGI server instead.
 	* Debug mode: on
 	* Restarting with stat
 	* Debugger is active!
 	* Debugger PIN: 886-099-577
 	* Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
14. Add a method About() to the file flaskblog.py decorated with route(\about) to render the "About" page.
15. Check the URL : http://localhost:5000/about

=========================================================================================================================================================
Flask : Lesson-2 Templates
=========================================================================================================================================================
1. Create a folder "templates" under the current working directory
   C:\Users\HP\DevEnv\Projects\VirtualEnvironment\Flask_Blog\templates
2. Create two html files Home.html and About.html
3. Modify the method Home() and About() to render the html files accordingly in the flaskblog.py.
4. Check the URL : http://localhost:5000/about to confirm.
5. Check code in home.html;about.html;flaskblog.py to understand template rendering.