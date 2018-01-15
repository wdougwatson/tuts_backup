Running a simple local HTTP server
To get around the problem of async requests, we need to test such examples by running them through a local web server. One of the easiest ways to do this for our purposes is to use Python's SimpleHTTPServer module.

To do this:

Install Python. If you are using Linux or Mac OS X, it should be available on your system already. If you are a Windows user, you can get an installer from the Python homepage and follow the instructions to install it:

Go to python.org
Under the Download section, click the link for Python "3.xxx".
At the bottom of the page, choose the Windows x86 executable installer and download it.
When it has downloaded, run it.
On the first installer page, make sure you check the "Add Python 3.xxx to PATH" checkbox.
Click Install, then click Close when the installation has finished.
Open your command prompt (Windows)/terminal (OS X/Linux). To check Python is installed, enter the following command:

python -V
This should return a version number. If this is OK, navigate to the directory that your example is inside, using the cd command.

# include the directory name to enter it, for example
cd Desktop
# use two dots to jump up one directory level if you need to
cd ..
Enter the command to start up the server in that directory:

# If Python version returned above is 3.X
python -m http.server
# If Python version returned above is 2.X
python -m SimpleHTTPServer
By default, this will run the contents of the directory on a local web server, on port 8000. You can go to this server by going to the URL localhost:8000 in your web browser. Here you'll see the contents of the directory listed — click the HTML file you want to run.