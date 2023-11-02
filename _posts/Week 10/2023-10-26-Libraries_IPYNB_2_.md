---
comments: True
layout: post
title: Daily Plan
description: my daily plan for the week
type: hacks
courses: {'compsci': {'week': 10}}
---
<strong><font size = 26>Learning Objectives:</font></strong><br><br>
- Select approproate libraries or existing code segments to use in creating new programs

<strong><font size = 26>What are Libraries?</font></strong><br><br>
In Python, a library is a collection of pre-written code, functions, and modules that extend the language's capabilities. These libraries are designed to be reused by developers to perform common tasks, rather than having to write the code from scratch. Libraries are essential for simplifying and accelerating the development process, as they provide a wide range of tools and functions for various purposes.

Here are some key points about Python libraries:

1. Modules: Libraries in Python consist of modules, which are individual Python files containing functions, classes, and variables related to a specific set of tasks or a particular domain. You can import these modules into your own Python code to access their functionality.

2. Standard Library: Python comes with a comprehensive standard library that includes modules for various tasks, such as working with files, networking, data processing, and more. These modules are readily available and do not require installation.

3. Third-party Libraries: In addition to the standard library, there is a vast ecosystem of third-party libraries created by the Python community. These libraries cover a wide range of domains, including web development, data analysis, machine learning, game development, and more. Some popular third-party libraries include NumPy, Pandas, Matplotlib, TensorFlow, Django, Flask, and many others.

<strong><font size = 26>How Do We Get Libraries into Our Code and Working?</strong></font><br><br>
To get libraries into our code, we use the import statement followed by the library we want to import. <br>Lets start simply:

> 


```python
#In this code cell, we are importing the math library which allows us to do math operations,
#and the random library which lets us take pseudorandom numbers and choices.
import math
import random
#We use the libraries by first calling them by their name, then using one of their methods.
#For example:
num = 64
print(math.sqrt(num))
numList = [1,2,3,4,5,6]
print(random.choice(numList))
#Here, 'math' and 'random' are the names of the libraries, and 'sqrt' and 'choice' are the names of the methods.
```

<font size = 5>We can also import parts of libraries by adding a "from" in front of our import.</font><br>



```python
from math import sqrt
from random import *
num = 64
print(sqrt(num))
numList = [1,2,3,4,5,6]
print(choice(numList))
```

<font size = 5>Now, we don't have to use math. in front of sqrt, and can just use the function by itself. We can also import *, or all, which makes it so that everything is imported. Here, we don't have to use random in front of choice, even though we didn't import choice specifically.

<strong><font size = 13>Popcorn Hack #1</font><br></strong><br><br>
<font size = 6>Import your own library from a list of provided libraries, and use one of its methods. This can be something very bare bones, such as printing the time, getting a random number in a list, or doing something after sleeping a certain amount of time



```python
#math library module examples: sqrt(num), square(num), cube(num), factorial(num)
#random library module examples: choice(list), randrange(lowest, highest, step[numbers chosen in multiples of {step}])
#datetime library module examples: datetime.now()
#sleep library module examples: sleep(milliseconds)

# example 1
from datetime import datetime
print(datetime.now())

# extra example
def cube(num):
    return num ** 3
num = 5  
result = cube(num)
print(result)


```

    2023-10-28 12:33:05.340577
    125


<strong><font size = 26>Documentation</strong></font><br><br>
Documentation in Python libraries refers to the written information and explanations provided to help users understand how to use the library, its classes, functions, and modules. It serves as a comprehensive guide that documents the library's functionality, usage, and often includes code examples. Documentation is typically created by the library developers and is an essential component of a well-maintained library.

<br>

Examples of Documentation: An introductory section explaining the purpose of the library, a section on how to install the library, basic usage examples, etc. 


```python
calcAverage(grades)

'''
You know the name of the procedure and the perameters, but...
You probably wouldn't be able to use this procedure 
with confidence because you don't know its function 
exactly (maybe you can guess that it finds the average, 
but you wouldn't know if it uses mean, mode, or median to 
find the average). You would also need more information on the
perameters.
'''
```

<strong><font size = 26>Libraries and APIs</strong></font><br><br>
- A file that contains procedures that cane be used in a program is called a <strong>library</strong>
- An <strong>Application Program Interface (API)</strong> provides specifications for how procedures in a library behave and can be used. 

APIs define the methods and functions that are available for developers to interact with a library. They specify how to make requests, provide inputs, and receive outputs, creating a clear and consistent way to use library features.

<strong><font size = 26>Which libraries will be very important to us?</font><br><br></strong>
<ul>
<li>Requests - Simplifies working with HTTP servers, including 'request'-ing data from them, and recieving it</li>
<li>Pillow - Simplifies image processing</li>
<li>Pandas - Simplifies data analysis & manipulation</li>
<li>Numpy - Vastly quickens functionality of arrays up to 50 times faster than regular python list</li>
<li>Scikit-Learn - Implements machine learning models and statistical modelling</li>
<li>Tensorflow - Data automation, model tracking, performance monitoring, and model retraining</li>
<li>Matplotlib - Creates static, animated, and interactive visualizations in Python</li>
</ul>
<h1> DON'T FORGET TO DOWNLOAD ALL OF THESE (pip install "library")</h1>

<strong><font size = 13>Popcorn Hack #2</font><br></strong><br><br>
<font size = 6>Using the requests library and the ? module (since we should already be using this in our backend) <strong>GET</strong> a request from the api at "https://api.github.com"



```python
import requests
#GET a request using the requests library. Remember to put your api link in quotes! If you get something along the lines of response [200] then you succeeded

requests.get("https://api.github.com")
```




    <Response [200]>



## Scikit-Learn and Numpy
This code uses NumPy to create an array, and Scikit-Learn to analyze the data. It creates a linear regression which describes the relationship between the x and y arrays which reperesent independent and dependent variables. In simpler terms, it is creating a line of best fit between the two data sets, just like how you would in something like desmos.

>



```python
import numpy as np
import numpy as np
from sklearn.linear_model import LinearRegression
from sklearn.model_selection import train_test_split
from sklearn.metrics import mean_squared_error

# Generate some example data
X = np.array([1, 2, 3, 4, 5]).reshape(-1, 1)  # Feature (independent variable)
y = np.array([2, 4, 5, 4, 5])             # Target (dependent variable)

# Split the data into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Create a Linear Regression model
model = LinearRegression()

# Fit the model to the training data
model.fit(X_train, y_train)

# Make predictions on the test data
y_pred = model.predict(X_test)

# Evaluate the model by calculating the Mean Squared Error  
mse = mean_squared_error(y_test, y_pred)

# Print the model coefficients and MSE, model coefficient is the slope of the linear regression line, MSE is how well the model is performing, the closer it is to 0 the better
print("Model Coefficients:", model.coef_)
print("Mean Squared Error:", mse)

intercept = model.intercept_
slope = model.coef_[0]
print(f"Linear Regression Equation: y = {intercept} + {slope} * X")


```

    Model Coefficients: [0.68571429]
    Mean Squared Error: 0.7346938775510206
    Linear Regression Equation: y = 1.7714285714285714 + 0.6857142857142857 * X


## Request
- The requests module allows you to send HTTP requests using Python.
- In order to download requests, you would have to type pip install requests in your terminal.

## Syntax
- requests.methodname(params)


```python
import requests

x = requests.get('http://127.0.0.1:9008/')

print(x.text)
#not functional code, example of syntax
```


    ---------------------------------------------------------------------------

    ConnectionRefusedError                    Traceback (most recent call last)

    File /opt/homebrew/lib/python3.11/site-packages/urllib3/connection.py:159, in HTTPConnection._new_conn(self)
        158 try:
    --> 159     conn = connection.create_connection(
        160         (self._dns_host, self.port), self.timeout, **extra_kw
        161     )
        163 except SocketTimeout:


    File /opt/homebrew/lib/python3.11/site-packages/urllib3/util/connection.py:84, in create_connection(address, timeout, source_address, socket_options)
         83 if err is not None:
    ---> 84     raise err
         86 raise socket.error("getaddrinfo returns an empty list")


    File /opt/homebrew/lib/python3.11/site-packages/urllib3/util/connection.py:74, in create_connection(address, timeout, source_address, socket_options)
         73     sock.bind(source_address)
    ---> 74 sock.connect(sa)
         75 return sock


    ConnectionRefusedError: [Errno 61] Connection refused

    
    During handling of the above exception, another exception occurred:


    NewConnectionError                        Traceback (most recent call last)

    File /opt/homebrew/lib/python3.11/site-packages/urllib3/connectionpool.py:670, in HTTPConnectionPool.urlopen(self, method, url, body, headers, retries, redirect, assert_same_host, timeout, pool_timeout, release_conn, chunked, body_pos, **response_kw)
        669 # Make the request on the httplib connection object.
    --> 670 httplib_response = self._make_request(
        671     conn,
        672     method,
        673     url,
        674     timeout=timeout_obj,
        675     body=body,
        676     headers=headers,
        677     chunked=chunked,
        678 )
        680 # If we're going to release the connection in ``finally:``, then
        681 # the response doesn't need to know about the connection. Otherwise
        682 # it will also try to release it and we'll have a double-release
        683 # mess.


    File /opt/homebrew/lib/python3.11/site-packages/urllib3/connectionpool.py:392, in HTTPConnectionPool._make_request(self, conn, method, url, timeout, chunked, **httplib_request_kw)
        391 else:
    --> 392     conn.request(method, url, **httplib_request_kw)
        394 # Reset the timeout for the recv() on the socket


    File /opt/homebrew/Cellar/python@3.11/3.11.5/Frameworks/Python.framework/Versions/3.11/lib/python3.11/http/client.py:1286, in HTTPConnection.request(self, method, url, body, headers, encode_chunked)
       1285 """Send a complete request to the server."""
    -> 1286 self._send_request(method, url, body, headers, encode_chunked)


    File /opt/homebrew/Cellar/python@3.11/3.11.5/Frameworks/Python.framework/Versions/3.11/lib/python3.11/http/client.py:1332, in HTTPConnection._send_request(self, method, url, body, headers, encode_chunked)
       1331     body = _encode(body, 'body')
    -> 1332 self.endheaders(body, encode_chunked=encode_chunked)


    File /opt/homebrew/Cellar/python@3.11/3.11.5/Frameworks/Python.framework/Versions/3.11/lib/python3.11/http/client.py:1281, in HTTPConnection.endheaders(self, message_body, encode_chunked)
       1280     raise CannotSendHeader()
    -> 1281 self._send_output(message_body, encode_chunked=encode_chunked)


    File /opt/homebrew/Cellar/python@3.11/3.11.5/Frameworks/Python.framework/Versions/3.11/lib/python3.11/http/client.py:1041, in HTTPConnection._send_output(self, message_body, encode_chunked)
       1040 del self._buffer[:]
    -> 1041 self.send(msg)
       1043 if message_body is not None:
       1044 
       1045     # create a consistent interface to message_body


    File /opt/homebrew/Cellar/python@3.11/3.11.5/Frameworks/Python.framework/Versions/3.11/lib/python3.11/http/client.py:979, in HTTPConnection.send(self, data)
        978 if self.auto_open:
    --> 979     self.connect()
        980 else:


    File /opt/homebrew/lib/python3.11/site-packages/urllib3/connection.py:187, in HTTPConnection.connect(self)
        186 def connect(self):
    --> 187     conn = self._new_conn()
        188     self._prepare_conn(conn)


    File /opt/homebrew/lib/python3.11/site-packages/urllib3/connection.py:171, in HTTPConnection._new_conn(self)
        170 except SocketError as e:
    --> 171     raise NewConnectionError(
        172         self, "Failed to establish a new connection: %s" % e
        173     )
        175 return conn


    NewConnectionError: <urllib3.connection.HTTPConnection object at 0x103e45c50>: Failed to establish a new connection: [Errno 61] Connection refused

    
    During handling of the above exception, another exception occurred:


    MaxRetryError                             Traceback (most recent call last)

    File /opt/homebrew/lib/python3.11/site-packages/requests/adapters.py:439, in HTTPAdapter.send(self, request, stream, timeout, verify, cert, proxies)
        438 if not chunked:
    --> 439     resp = conn.urlopen(
        440         method=request.method,
        441         url=url,
        442         body=request.body,
        443         headers=request.headers,
        444         redirect=False,
        445         assert_same_host=False,
        446         preload_content=False,
        447         decode_content=False,
        448         retries=self.max_retries,
        449         timeout=timeout
        450     )
        452 # Send the request.
        453 else:


    File /opt/homebrew/lib/python3.11/site-packages/urllib3/connectionpool.py:726, in HTTPConnectionPool.urlopen(self, method, url, body, headers, retries, redirect, assert_same_host, timeout, pool_timeout, release_conn, chunked, body_pos, **response_kw)
        724     e = ProtocolError("Connection aborted.", e)
    --> 726 retries = retries.increment(
        727     method, url, error=e, _pool=self, _stacktrace=sys.exc_info()[2]
        728 )
        729 retries.sleep()


    File /opt/homebrew/lib/python3.11/site-packages/urllib3/util/retry.py:446, in Retry.increment(self, method, url, response, error, _pool, _stacktrace)
        445 if new_retry.is_exhausted():
    --> 446     raise MaxRetryError(_pool, url, error or ResponseError(cause))
        448 log.debug("Incremented Retry for (url='%s'): %r", url, new_retry)


    MaxRetryError: HTTPConnectionPool(host='127.0.0.1', port=9008): Max retries exceeded with url: / (Caused by NewConnectionError('<urllib3.connection.HTTPConnection object at 0x103e45c50>: Failed to establish a new connection: [Errno 61] Connection refused'))

    
    During handling of the above exception, another exception occurred:


    ConnectionError                           Traceback (most recent call last)

    Cell In[10], line 3
          1 import requests
    ----> 3 x = requests.get('http://127.0.0.1:9008/')
          5 print(x.text)
          6 #not functional code, example of syntax


    File /opt/homebrew/lib/python3.11/site-packages/requests/api.py:75, in get(url, params, **kwargs)
         64 r"""Sends a GET request.
         65 
         66 :param url: URL for the new :class:`Request` object.
       (...)
         71 :rtype: requests.Response
         72 """
         74 kwargs.setdefault('allow_redirects', True)
    ---> 75 return request('get', url, params=params, **kwargs)


    File /opt/homebrew/lib/python3.11/site-packages/requests/api.py:60, in request(method, url, **kwargs)
         56 # By using the 'with' statement we are sure the session is closed, thus we
         57 # avoid leaving sockets open which can trigger a ResourceWarning in some
         58 # cases, and look like a memory leak in others.
         59 with sessions.Session() as session:
    ---> 60     return session.request(method=method, url=url, **kwargs)


    File /opt/homebrew/lib/python3.11/site-packages/requests/sessions.py:533, in Session.request(self, method, url, params, data, headers, cookies, files, auth, timeout, allow_redirects, proxies, hooks, stream, verify, cert, json)
        528 send_kwargs = {
        529     'timeout': timeout,
        530     'allow_redirects': allow_redirects,
        531 }
        532 send_kwargs.update(settings)
    --> 533 resp = self.send(prep, **send_kwargs)
        535 return resp


    File /opt/homebrew/lib/python3.11/site-packages/requests/sessions.py:646, in Session.send(self, request, **kwargs)
        643 start = preferred_clock()
        645 # Send the request
    --> 646 r = adapter.send(request, **kwargs)
        648 # Total elapsed time of the request (approximately)
        649 elapsed = preferred_clock() - start


    File /opt/homebrew/lib/python3.11/site-packages/requests/adapters.py:516, in HTTPAdapter.send(self, request, stream, timeout, verify, cert, proxies)
        512     if isinstance(e.reason, _SSLError):
        513         # This branch is for urllib3 v1.22 and later.
        514         raise SSLError(e, request=request)
    --> 516     raise ConnectionError(e, request=request)
        518 except ClosedPoolError as e:
        519     raise ConnectionError(e, request=request)


    ConnectionError: HTTPConnectionPool(host='127.0.0.1', port=9008): Max retries exceeded with url: / (Caused by NewConnectionError('<urllib3.connection.HTTPConnection object at 0x103e45c50>: Failed to establish a new connection: [Errno 61] Connection refused'))



```python
import requests

# Replace this URL with the website you want to request
url = 'https://www.example.com'

# Send a GET request to the URL
response = requests.get(url)

# Check if the request was successful (status code 200)
if response.status_code == 200:
    # Print the content of the response (the HTML content of the webpage)
    print(response.text)
else:
    # If the request was not successful, print an error message
    print(f"Failed to retrieve the page. Status code: {response.status_code}")

```

    <!doctype html>
    <html>
    <head>
        <title>Example Domain</title>
    
        <meta charset="utf-8" />
        <meta http-equiv="Content-type" content="text/html; charset=utf-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1" />
        <style type="text/css">
        body {
            background-color: #f0f0f2;
            margin: 0;
            padding: 0;
            font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", "Open Sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
            
        }
        div {
            width: 600px;
            margin: 5em auto;
            padding: 2em;
            background-color: #fdfdff;
            border-radius: 0.5em;
            box-shadow: 2px 3px 7px 2px rgba(0,0,0,0.02);
        }
        a:link, a:visited {
            color: #38488f;
            text-decoration: none;
        }
        @media (max-width: 700px) {
            div {
                margin: 0 auto;
                width: auto;
            }
        }
        </style>    
    </head>
    
    <body>
    <div>
        <h1>Example Domain</h1>
        <p>This domain is for use in illustrative examples in documents. You may use this
        domain in literature without prior coordination or asking for permission.</p>
        <p><a href="https://www.iana.org/domains/example">More information...</a></p>
    </div>
    </body>
    </html>
    


## Pillow
- Pillow is a imaging library that provides easy-to-use methods to include, change, save different image formats.
- To dowload pillow onto your computer, you would enter the command pip install Pillow into your terminal.



```python
from PIL import Image, ImageDraw, ImageFont

# Create a new blank image
width, height = 400, 200
image = Image.new("RGB", (width, height), "white")

# Create an ImageDraw object
draw = ImageDraw.Draw(image)

# Draw a red line from (50, 50) to (350, 150)
line_color = (255, 0, 0)  # Red color
draw.line((50, 50, 350, 150), fill=line_color, width=3)

# Add text to the image
text = "This was created using Pillow!"
text_color = (0, 0, 0)  # Black color
font_size = 20
font = ImageFont.load_default()  # Use a default font
text_position = (50, 160) 
draw.text(text_position, text, fill=text_color, font=font)

# Save or display the image
image.show()
image.show()
#This opens the image in your default image viewer and when you stop the code, it will return an error, but don't worry about that

```


```python
from PIL import Image

# Open an image
original_image = Image.open('image.png') #replace image.png with valid image

# Display information about the image
width, height = original_image.size
format = original_image.format
print(f"Original Image Size: {width}x{height}")
print(f"Original Image Format: {format}")

# Resize the image to a new size
new_size = (width // 2, height // 2)  # Reduce the size by half
resized_image = original_image.resize(new_size)

# Save the resized image
resized_image.save('resized_image.jpg')

# Display information about the resized image
resized_width, resized_height = resized_image.size
print(f"Resized Image Size: {resized_width}x{resized_height}")

# Show both the original and resized images
original_image.show()
resized_image.show()

```


    ---------------------------------------------------------------------------

    FileNotFoundError                         Traceback (most recent call last)

    c:\Users\matth\librarylesson\lessons\2023-10-26-Libraries.ipynb Cell 26 line 4
          <a href='vscode-notebook-cell:/c%3A/Users/matth/librarylesson/lessons/2023-10-26-Libraries.ipynb#X44sZmlsZQ%3D%3D?line=0'>1</a> from PIL import Image
          <a href='vscode-notebook-cell:/c%3A/Users/matth/librarylesson/lessons/2023-10-26-Libraries.ipynb#X44sZmlsZQ%3D%3D?line=2'>3</a> # Open an image
    ----> <a href='vscode-notebook-cell:/c%3A/Users/matth/librarylesson/lessons/2023-10-26-Libraries.ipynb#X44sZmlsZQ%3D%3D?line=3'>4</a> original_image = Image.open('image.png')
          <a href='vscode-notebook-cell:/c%3A/Users/matth/librarylesson/lessons/2023-10-26-Libraries.ipynb#X44sZmlsZQ%3D%3D?line=5'>6</a> # Display information about the image
          <a href='vscode-notebook-cell:/c%3A/Users/matth/librarylesson/lessons/2023-10-26-Libraries.ipynb#X44sZmlsZQ%3D%3D?line=6'>7</a> width, height = original_image.size


    File c:\Users\matth\AppData\Local\Programs\Python\Python311\Lib\site-packages\PIL\Image.py:3243, in open(fp, mode, formats)
       3240     filename = fp
       3242 if filename:
    -> 3243     fp = builtins.open(filename, "rb")
       3244     exclusive_fp = True
       3246 try:


    FileNotFoundError: [Errno 2] No such file or directory: 'image.png'


## Pandas
This code utilizes pandas in the DataFrame form to organize the data in to a table with the categories on the horizontal axis and their values on the vertical. Pandas creates a way for the user to organize data in a much simpler form and in different styles depending on what the user wants


```python
#This code utilizes pandas which is a way for you as a user, to create data tables that are much more organized

#imports pandas so it's able to be used
import pandas as pd

#data is created and will be sorted from left to right into top to bottom
data = {'Name': ['Matthew', 'Lindsay', 'Josh', 'Ethan'],
        'Grade': [97, 92, 90, 80]}

#defines a variable and utilizes pandas by using a DataFrame for the data
df = pd.DataFrame(data)
#tbere are other forms other than DataFrame, those are Series (single Column), Panel (3D), Multindex (multiple levels of index), and Categorical (categories), 
#increase the side count by one
df.index += 1

print(df)

```

          Name  Grade
    1  Matthew     97
    2  Lindsay     92
    3     Josh     90
    4    Ethan     80


Another example code, this time utilizing both numpy and pandas


```python
import pandas as pd
import numpy as np

# Sample data
data = {
    'Grade': ['A', 'B', 'A', 'C', 'B', 'C', 'A', 'B', 'A'],
    'Percent': [94, 82, 91, 76, 89, 79, 92, 87, 99]
}

# Create a Pandas DataFrame
df = pd.DataFrame(data)

# Calculate the mean of each Grade using NumPy
means = df.groupby('Grade')['Percent'].mean().reset_index()

# Organize the results into a new data table
result = pd.DataFrame({'Grade': ['A', 'B', 'C'], 'Mean Grade': means['Percent']})

result.index += 1
# Display the result
print(result)

```

      Grade  Mean Grade
    1     A        94.0
    2     B        86.0
    3     C        77.5


## TensorFlow
The provided code demonstrates a basic example of linear regression using TensorFlow and Keras. It begins by importing the necessary libraries, TensorFlow and NumPy. It then generates a synthetic dataset with 1000 samples, where the input features are random, and the target values are computed as a linear combination of the input features with added noise. A data pipeline is set up using TensorFlow, which includes shuffling and batching the data for efficient processing. A simple linear regression model is defined using Keras, consisting of one dense layer. The model is compiled with the Adam optimizer and mean squared error as the loss function. It is then trained on the synthetic data for ten epochs. After training, the model is used to make predictions on new data points, and the predictions are printed to the console. This code provides a basic illustration of how to perform a simple machine learning task with TensorFlow, from data generation to model training and prediction.


```python
import tensorflow as tf
import numpy as np

# Create a synthetic dataset
num_samples = 1000
input_data = np.random.rand(num_samples, 2)
target_data = input_data[:, 0] * 2 + input_data[:, 1] * 3 + np.random.randn(num_samples)

# Define a data pipeline using TensorFlow
dataset = tf.data.Dataset.from_tensor_slices((input_data, target_data))
dataset = dataset.shuffle(buffer_size=num_samples)
dataset = dataset.batch(32)
dataset = dataset.prefetch(buffer_size=tf.data.AUTOTUNE)

# Create a simple linear regression model using Keras
model = tf.keras.Sequential([
    tf.keras.layers.Dense(1, input_shape=(2,))
])
model.compile(optimizer='adam', loss='mean_squared_error')

# Train the model on the synthetic data
model.fit(dataset, epochs=10)

# Generate predictions
new_data = np.array([[0.5, 0.7], [0.3, 0.2]])
predictions = model.predict(new_data)
print("Predictions:", predictions)

```


    ---------------------------------------------------------------------------

    KeyboardInterrupt                         Traceback (most recent call last)

    Cell In[14], line 1
    ----> 1 import tensorflow as tf
          2 import numpy as np
          4 # Create a synthetic dataset


    File /opt/homebrew/lib/python3.11/site-packages/tensorflow/__init__.py:38
         35 import sys as _sys
         36 import typing as _typing
    ---> 38 from tensorflow.python.tools import module_util as _module_util
         39 from tensorflow.python.util.lazy_loader import LazyLoader as _LazyLoader
         41 # Make sure code inside the TensorFlow codebase can use tf2.enabled() at import.


    File /opt/homebrew/lib/python3.11/site-packages/tensorflow/python/__init__.py:36
         27 import traceback
         29 # We aim to keep this file minimal and ideally remove completely.
         30 # If you are adding a new file with @tf_export decorators,
         31 # import it in modules_with_exports.py instead.
         32 
         33 # go/tf-wildcard-import
         34 # pylint: disable=wildcard-import,g-bad-import-order,g-import-not-at-top
    ---> 36 from tensorflow.python import pywrap_tensorflow as _pywrap_tensorflow
         38 # pylint: enable=wildcard-import
         39 
         40 # from tensorflow.python import keras
         41 # from tensorflow.python.layers import layers
         42 from tensorflow.python.saved_model import saved_model


    File /opt/homebrew/lib/python3.11/site-packages/tensorflow/python/pywrap_tensorflow.py:26
         21 from tensorflow.python.platform import self_check
         23 # TODO(mdan): Cleanup antipattern: import for side effects.
         24 
         25 # Perform pre-load sanity checks in order to produce a more actionable error.
    ---> 26 self_check.preload_check()
         28 # pylint: disable=wildcard-import,g-import-not-at-top,unused-import,line-too-long
         30 try:
         31   # This import is expected to fail if there is an explicit shared object
         32   # dependency (with_framework_lib=true), since we do not need RTLD_GLOBAL.


    File /opt/homebrew/lib/python3.11/site-packages/tensorflow/python/platform/self_check.py:63, in preload_check()
         50       raise ImportError(
         51           "Could not find the DLL(s) %r. TensorFlow requires that these DLLs "
         52           "be installed in a directory that is named in your %%PATH%% "
       (...)
         56           "https://support.microsoft.com/help/2977003/the-latest-supported-visual-c-downloads"
         57           % " or ".join(missing))
         58 else:
         59   # Load a library that performs CPU feature guard checking.  Doing this here
         60   # as a preload check makes it more likely that we detect any CPU feature
         61   # incompatibilities before we trigger them (which would typically result in
         62   # SIGILL).
    ---> 63   from tensorflow.python.platform import _pywrap_cpu_feature_guard
         64   _pywrap_cpu_feature_guard.InfoAboutUnusedCPUFeatures()


    KeyboardInterrupt: 


## Matplotlib
The provided Python code demonstrates the basic usage of Matplotlib, a popular library for creating data visualizations. In this example, we start by importing the Matplotlib's pyplot module, often aliased as plt. We define some sample data as lists for the X and Y values. Then, we create a figure and an axis object using plt.subplots(). Next, we plot the data points on the graph with ax.plot(x, y) and set a label for the line. We also add labels for the X and Y axes and set a title for the plot. To provide context for the plot, we include a legend with the label we set earlier. Finally, plt.show() is called to display the graph. When you run this code, it will generate a simple line plot displaying the data points with appropriate labels, a title, and a legend, making it a clear and informative visualization.


```python
import matplotlib.pyplot as plt

# Sample data
x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

# Create a figure and axis
fig, ax = plt.subplots()

# Plot the data
ax.plot(x, y, label='Linear Line')

# Set labels and title
ax.set_xlabel('X-axis')
ax.set_ylabel('Y-axis')
ax.set_title('Simple Line Plot')

# Add a legend
ax.legend()

# Display the plot
plt.show()

```


    
![png](output_32_0.png)
    


<h1>Homework Hack</h1> 
1) Create a code that makes a data table which organizes the average values(mean) from a data set the has atleast 5 values per category and using 2 libraries, ex: <br></br>
2) Create a Python script that downloads images from a website using the requests library, processes them with the Pillow library, and then performs data analysis with the Pandas library.


```python
#homework 1

import pandas as pd
import numpy as np

data = {
    'Category': ['A', 'A', 'A', 'A', 'A', 'B', 'B', 'B', 'B', 'B'],
    'Values': [5, 8, 9, 7, 2, 1, 4, 3, 12, 15]
}

# Create a Pandas DataFrame
df = pd.DataFrame(data)

if df['Category'].value_counts().min() < 5:
    raise ValueError("There must be at least 5 values per category.")

# Calculate the mean of each category
mean_values = df.groupby('Category')['Values'].mean()

# Create a new DataFrame for the means
mean_df = pd.DataFrame(mean_values).reset_index()

# Print the resulting data table
print(mean_df)

```

      Category  Values
    0        A     6.2
    1        B     7.0



```python
#homework 2

import requests
from PIL import Image
import pandas as pd
from io import BytesIO  

image_url = 'https://upload.wikimedia.org/wikipedia/en/d/d7/Harry_Potter_character_poster.jpg'

response = requests.get(image_url)
img = Image.open(BytesIO(response.content)) 

img = img.convert('L')

data = {'Pixel Values': list(img.getdata())}
df = pd.DataFrame(data)

print(df.head())

```

       Pixel Values
    0            77
    1            78
    2            76
    3            79
    4            79

