Contents
=================

* [Data Structure](#data-structure)
  * [list](#list)
  * [tuple](#tuple)
  * [dictionary](#dictionary)
  * [set](#set)
* [Contorl Program Flow](#contorl-program-flow)
  * [Choice Workflow](#choice-workflow)
  * [Repeation Workflow](#repeation-workflow)
  * [Function](#function)
  * [Small Project](#small-project)
* [Python Environment](#python-environment)
  * [pip](#pip)
  * [virtualenv](#virtualenv)
* [Python Module](#python-module)
* [Python Package](#python-package)
* [Object Oriented Programming](#object-oriented-programming)
* [Decorator](#decorator)
* [File IO](#file-io)
* [Exception](#exception)
* [Commandlne Argument](#commandlne-argument)
* [Testing](#testing)
* [Practice](#practice)
* [List Comprehension](#list-comprehension)
* [Generator](#generator)
* [HTTP Networking](#http-networking)
* [JSON Manipulation](#json-manipulation)
* [Muti\-threading](#muti-threading)
* [Queue](#queue)
* [Python Toolbox](#python-toolbox)
  * [Requests](#requests)
  * [BeautifulSoup](#beautifulsoup)
  * [Practice](#practice-1)
  * [Jupyter](#jupyter)
  * [Numpy](#numpy)
  * [Pandas](#pandas)
  * [Matplotlib](#matplotlib)
  * [Flask](#flask)

----

# Data Structure

## list

``` python
# 声明一个list
a = []
a = [1, 2, 3, 4, 5]
print(type(a))
b = [6, 7, 8, 9]
# list支持的operation
c = a  + b
print(c)
# list的插入和删除
a.insert(0, 0)
print(a)
b.append(10)
print(b)
del a[1]
print(a)
```

## tuple

``` python
# 声明一个tuple
a = ()
a = (1, 2 ,3, 4)
b = (3, 4, 5)
print(a)
## tuple和list不同的是，tuple创建之后不支持更改
a[0] = 1
```

## dictionary

```python
# 声明一个dict
a = {}
a = {
    'Course': 'Python',
    'name': 'xiaolongge'
}
print(a)
# 根据Key可以获得Value
print(a['Course'])
# 使用get方法获得Value，如果不存在为空
print(a.get('Course'))
# 增加key-value
a['phone'] = '111111'
print(a)
# 删除
del a['phone']
print(a)
```

## set

``` python
# 声明一个set
a = set()
a = set([1, 2, 3, 4, 5])
print(type(a))
## set和list不同的是，set里面的元素是不能重复的
b = set([3, 3, 4, 5, 6])
print(b)
# set可以不可能直接索引访问，需要转换为list再索引
print(list(b)[0])
# 从而也可以实现insert和appen操作
list(b).insert(0, 2)
list(a).append(6)
# 删除操作
del list(a)[0]
print(a)
# set可以实现数学集合中的并集和交集的操作
print(a | b)
print(a & b)
```

# Contorl Program Flow

## Choice Workflow
``` python
a = 1
if a == 1:
        print('Value of a is 1')
elif a > 1:
        print('Value of a bigger than 1')
else:
    print('Value of a smaller than 1')
```

## Repeation Workflow

``` python
# print something then times
for i in range(11):
    print('%d: Python' % i)
# also, you can use while keyword to implement this function
a = 10
while a > 0:
    print('%d: Python' % a)
    a -= 1
```
## Function

``` python
# python函数用def keyword来定义
def fun():
    print('this is a function')
fun()
# python函数可以返回多个返回值，组织为一个tuple
def return_fun():
    return 'one', 'two'
a, b = return_fun()
print(a)
print(b)
```

## Small Project
实现一个计算机，用户输入两个数字，返回两个数字的和
``` python  
def add(a, b):
    if type(a) is int and type(b) is int:
        print(a + b)
    else:
        print('input is not int type')

num1 = input('Please input a int number: ')
num2 = input('Please input anthor int number: ')
add(num1, num2)
```

# Python Environment
## pip
Python下的包管理工具
``` shell
pip install pytest
pip ---version
pip list
pip freeze > requirement.txt
```

## virtualenv
Python虚拟环境
``` shell
pip install virtualenv
virtualenv env  
```
# Python Module

``` python
def add(a, b):
    if type(a) is int and type(b) is int:
        print(a + b)
    else:
        print('input is not int type')
```

``` python
import calcuator
# from calcuator import add
num1 = input('Please input a int number: ')
num2 = input('Please input anthor int number: ')
add(num1, num2)
```

# Python Package

if there is a file named __init__.py, then Python will see it as a package
``` shell
Schedule
|-  __init__.py
|- schedule.py
```

# Object Oriented Programming

``` python
# 声明一个class
class Schedule(object):

    name = None
    desp = None
    tasks = {}

    # 构造函数
    def __init__(self, n, d):
        self.name = n
        self.desp = d
    
    # method
    def add_task(self, name, content, priority):
        if name not in self.tasks:
            task = [name, content, priority]
            self.tasks.update({name: task})
        self.display()
        
    def remove_task(self, name):
        if name in self.tasks:
            self.tasks.pop(name, None)
        self.display()

    def display(self):
        if self.tasks:
            print('here are you tasks')
            for v in self.tasks.values():
                print('%-10s %-5s %-50s'% (v[0], v[2], v[1]))

    def __str__(self):
        return 'Schedule %s, %s' % (self.name, self.desp)

s1 = Schedule('s1', 'work schedule')
s1.add_task('cs105', 'study cs105 course', 1000)
s1.add_task('cs106', 'study cs106 course', 2000)
```

# Decorator 
Python中函数也视作为一个对象，所以可以作为参数
``` python
def answer_to_university():
    
    def give_42():
        return 42
    
    return give_42

answer = answer_to_university()
print(answer_to_university)
print(answer_to_university())
print(answer_to_university()())
print(answer())
```

``` python
from datetime import datetime

def display_decorator(func):

    def wrapper(*args, **kwargs):
        print(str(datetime.now()))
        return func(*args, **kwargs)

    return wrapper

class Schedule(object):

    name = None
    desp = None
    tasks = {}

    def __init__(self, n, d):
        self.name = n
        self.desp = d

    @display_decorator
    def add_task(self, name, content, priority):
        if name not in self.tasks:
            task = [name, content, priority]
            self.tasks.update({name: task})
        self.display()

    @display_decorator
    def remove_task(self, name):
        if name in self.tasks:
            self.tasks.pop(name, None)
        self.display()

    def display(self):
        if self.tasks:
            print('here are you tasks')
            for v in self.tasks.values():
                print('%-10s %-5s %-50s'% (v[0], v[2], v[1]))

    def __str__(self):
        return 'Schedule %s, %s' % (self.name, self.desp)

s1 = Schedule('s1', 'work schedule')
s1.add_task('cs105', 'study cs105 course', 1000)
s1.add_task('cs106', 'study cs106 course', 2000)
```
# File IO

``` python
with open('test.txt', 'r') as f:
    data = f.read()
    print(data)
```

# Exception

``` python
try:
    # code with error
exception Exception as e:
    # do somethings
finally:
    # finally do somethins
```
also, you can define your exception classes
``` python
class AwesomeException(Exception):
    def __init__(self, *args, **kvargs):
        Exception.__init__(self, *args, **kvargs)

raise AwesomeException('somwhow,   this is an awesome exception')
```

# Commandlne Argument

``` python 
if __name__ == '__main__'
    args = sys.argv
    a1 = args[1]
    a2 = args[2]
```

# Testing

``` python
from schedule import Schedule

def test_add():
    s = Schedule('s1', 'study schedule')
    s.add_task('cs105', 'study python course', 100)
    assert 'cs105' in s.tasks

def test_remove():
    s = Schedule('s1', 'study schedule')
    s.remove_task('cs105')
    assert s.tasks == {}
```

# Practice

``` python
import sys
import os
import json
from datetime import datetime

PATH = os.path.abspath('schedule.json')



class Schedule(object):

    name = None
    desp = None

    def __init__(self):
        if os.path.exists(PATH):
            with open(PATH, 'r') as f:
                data = f.read()
                self.tasks = json.loads(data)
        else:
            self.tasks = {}

    def add_task(self, name, content, priority):
        if name not in self.tasks:
            task = [name, content, priority]
            self.tasks.update({name: task})
        self.display()
        self.flushToFile()

    def remove_task(self, name):
        if name in self.tasks:
            self.tasks.pop(name, None)
        self.display()
        self.flushToFile()

    def display(self):
        if self.tasks:
            print('Here are you tasks: ')
            for v in self.tasks.values():
                print('%-10s %-5s %-50s'% (v[0], v[2], v[1]))

    def flushToFile(self):
        data = json.dumps(self.tasks)
        with open(PATH, 'w+') as f:
            f.write(data)

    def __str__(self):
        return 'Schedule %s, %s' % (self.name, self.desp)

if __name__ == '__main__':
    args = sys.argv

    if len(args) < 3:
        print('Usage: schedule.py option[ add | move ] parameters...')
        exit()

    opt = args[1]
    parameter = args[2:]
    sch = Schedule()

    if opt == 'add':
        # add_task
        if len(parameter) < 3:
            print('add need 3 parameters[ name content priority ]')
            exit()

        sch.add_task(parameter[0], parameter[1], parameter[2])

    elif opt == 'remove':
        # remove_task
        if len(parameter) < 1:
            print('remove need schedult name')
            exit()

        sch.remove_task(parameter[0])

    else:
        print('Invalid option [ add | remove ]')
        exit()
```

later

# List Comprehension

``` python
# variable = [do something condition]
a = [1, 2, 3, 4, 5, 6]
result = [x for x in a if x < 3]
print(result)
result2 = {x for x in a if x < 3}
print(result2)
b = ['a', 'b']
result3 = {x:y for x in a for y in b}
print(result3)
```

# Generator

``` python
x = [1, 2, 3, 4, 5]
gen = (i for i in x if i < 3)
print(type(gen))
# how to use generator
for i in gen:
    print(i)
```
``` python
vowels = 'aeiou'
sentence = 'Finally, you can try to quickly find non-vowel characters in a sentence.'
result = ''.join(c for c in sentence if c not in vowels)
print(result)
```
# HTTP Networking

``` python
import httplib

conn = httplib.HTTPConnection('jsonplaceholder.typicode.com')
conn.request('GET', '/posts')
resp = conn.getresponse()
data = resp.read()
print(data)
```

# JSON Manipulation

``` python
import httplib
import json

conn = httplib.HTTPConnection('jsonplaceholder.typicode.com')
conn.request('GET', '/posts')
resp = conn.getresponse()
data = resp.read()
parsed = json.loads(data)
print(parsed)
```

# Muti-threading
not use muti-threading
``` python
import httplib
import time
from datetime import datetime

def get_data(n):
    for i in range(n):
        time.sleep(1)
        conn = httplib.HTTPConnection('jsonplaceholder.typicode.com')
        conn.request('GET', '/posts')
        resp = conn.getresponse()
        data = resp.read()
start = datetime.now()
get_data(40)
end = datetime.now()
print('Total time: ' + str(end - start) )
```
use muti-threading
``` python
import httplib
import time
from datetime import datetime
import threading

def get_data(n):
    for i in range(n):
        time.sleep(1)
        conn = httplib.HTTPConnection('jsonplaceholder.typicode.com')
        conn.request('GET', '/posts')
        resp = conn.getresponse()
        data = resp.read()
        
start = datetime.now()
for i in range(4):
    t = threading.Thread(target=get_data, args={10, })
    t.start()
end = datetime.now()
print('Total time: ' + str(end - start) )
```

# Queue

``` python
import Queue

q = Queue.Queue()
for i in range(100):
    q.put(i)
    
while not q.empty():
    print(q.get())
```
``` python
import Queue
import threading
import random
import time

counter = 0
lock = threading.Lock()

q = Queue.Queue()

def worker(i, q):
    while True:
        task = q.get()
        print('%d working on tast: %d' % (i, task))
        time.sleep(1)
        count_new_tasks = random.randrange(0, 10)
        print('%d putting %d new tasks in queue' % (i, count_new_tasks))
        for new_task in range(count_new_tasks):
            q.put(new_task)
        q.task_done()
        global  counter
        with lock:
            counter += 1
            print('procceed %d tasks so far' % counter)

for i in range(2):
    t = threading.Thread(target=worker, args={i, q})
    t.start()

q.put(1)
q.join()
```

# Python Toolbox
## Requests

``` python
import requests

resp = requests.get('http://jsonplaceholder.typicode.com/posts')
parsed = resp.json()    
print(parsed)
```
## BeautifulSoup

``` python
import requests
from bs4 import BeautifulSoup

resp = requests.get('https://en.wikipedia.org/wiki/Main_Page')
soup = BeautifulSoup(resp.text, 'html.parser')

for a_link in soup.find_all('a'):
    print(a_link.get('href'))
```

##  Practice

``` python
import queue
import threading
import requests
import time
import re
from bs4 import BeautifulSoup

"""
+ 实现一个多线程爬虫程序
+ WikiCrawl(url, limit, nthread)
+ url： 爬虫入口的url
+ limit: 爬取链接的个数
+ nthread: 开启的线程数

"""

class WikiCrawl(object):

    url = None
    limit = None
    counter = None
    nthread = None
    q = queue.Queue()
    visited = set()
    lock = threading.Lock()

    def __init__(self, url, limit, n):
        self.url = url
        self.limit = limit
        self.counter = 0
        self.nthread = n

    def send_request(self, url):
        hashValue = hash(url)
        if hashValue not in self.visited:
            self.visited.add(hashValue)
            time.sleep(1)
            resp = requests.get(url)
            self.parse_link(resp.text, url)

    def parse_link(self, data, url):

        if self.counter >= self.limit:
            exit()

        soup = BeautifulSoup(data, 'html.parser')
        print('URL: ' + url + 'start to parse')

        for a_link in soup.find_all('a'):
            a_href = a_link.get('href')
            # 判断抓取的url是否合法
            if re.match(r'^https?:/{2}\w.+$', str(a_href)):
                self.q.put(a_href)
                print('The sub link is: ' + a_href)
                with self.lock:
                    if self.counter >= self.limit:
                        print('The crawler\'s work have done.')
                        print('Total page: %d' % self.counter)
                        exit()
                    self.counter += 1

    def worker(self):
        while True:
            if self.q.empty():
                self.send_request(self.url)
            else:
                self.send_request(self.q.get())

    def start(self):
        print('Now the crawler starts to work:')
        for i in range(self.nthread):
            t = threading.Thread(target=self.worker)
            t.start()


if __name__ == '__main__':
    crawl = WikiCrawl('https://en.wikipedia.org/wiki/Main_Page', 100, 4)
    crawl.start()

```

##  Jupyter

``` shell
pip install jupyter
jupyter notebook
```

## Numpy

``` shell
pip install numpy
```

``` python
import numpy as np

a = np.array([1, 2, 3])
print(type(a))
data = np.array([[1, 2, 3], [4, 5, 6]])
print(data)
print(data.shape)
print(np.zeros([3, 4]))
print(np.ones([3, 4]))
print(data[:, 1])
print(data[1, :])
print(data[:, :2])

quality = np.array(['Good', 'Bad', 'Good', 'Good'])
product = np.array(range(4))
print(product[quality == 'Good'])
```

## Pandas

``` shell
pip install pandas
```
``` python
from pandas import DataFrame
import pandas as pd

df = DataFrame({
    'name': ['CS105', 'CS106', 'CS107'],
    'course': ['python', 'java', 'data science']
})
print(df)
print(df.head())
print(df.columns)

print(df.iloc[1])
print(df.iloc[1:3])
print(df.iloc[1:3, 0:2])
print(df.name)
print(df.course)
print(df[df.course == 'python'])

groups = df.groupby('course')
print(groups.get_group('java'))

df2 = DataFrame({
    'name': ['CS105', 'CS106', 'CS107'],
    'student': [10, 20, 30]
})
print(pd.merge(df, df2))

df.to_csv('data.csv', encoding='utf-8')
new_df = pd.read_csv('data.csv')
print(new_df)
```
pandas-datareader
``` shell
pip install pandas-datareader
```
``` python
import pandas_datareader as web
import datetime

start = datetime.datetime(2017, 1, 1)
end = datetime.datetime(2017, 5, 30)

data = web.DataReader('AAPL', 'google', start, end)
print(data) 
```

## Matplotlib

``` shell
pip install matplotlib
```
``` python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

x = pd.period_range(datetime.datetime.now(), periods=200, freq='d')
x = x.to_timestamp().to_pydatetime()

y = np.random.randn(200, 3)
plt.plot(x, y)
plt.show()
```

``` python
import pandas_datareader as web
import datetime
import matplotlib.pyplot as plt

start = datetime.datetime(2017, 1, 1)
end = datetime.datetime(2017, 5, 30)

data = web.DataReader('AAPL', 'google', start, end)
data.plot(subplots = True, figsize = (8, 8))
plt.show()
```

## Flask

- blog.py
``` python
    from flask import (
    Flask,
    render_template,
    request,
    redirect,
    url_for,
    session
)

from datetime import datetime
from flask.ext.sqlalchemy import SQLAlchemy

app = Flask(__name__)
app.config.from_object('config')
db = SQLAlchemy(app)

class User(db.Model):
    id = db.Column(db.Integer, primary_key = True)
    username = db.Column(db.String(64), index = True, unique = True)
    password = db.Column(db.String(64))

class Post(db.Model):
    id = db.Column(db.Integer, primary_key = True)
    content = db.Column(db.String(600))
    timestamp = db.Column(db.DateTime)
    user_id = db.Column(db.Integer, db.ForeignKey('user.id'))

db.create_all()
db.session.commit()


"""
index
    - go to the signup
    - go to login
    - if already login find all the blog posts
    - if already login, go to create blog page

signup
    - create new user account
    - after create, redirect to index

login
    - a form to login
    - after login, redirect to index
    
logout {no html}
    - logout blog

create 
    - a form to create blog
    - after creation, redirect to index
"""

@app.route('/')
def index():
    blogs = Post.query.all()
    return render_template('index.html.jinjia', blogs = blogs)

@app.route('/signup', methods=['GET', 'POST'])
def signup():
    if request.method == 'POST':
        username = request.form['username']
        password = request.form['password']

        if username is '':
            return render_template('signup.html.jinjia', userAlert = 1)
        elif password is '':
            return render_template('signup.html.jinjia', passAlert = 1)
        else:
            user = User(username = username, password = password)
            db.session.add(user)
            db.session.commit()
            session['username'] = username
            return redirect(url_for('index'))
    return render_template('signup.html.jinjia')

@app.route('/login', methods=['GET', 'POST'])
def login():
    if request.method == 'POST':
        username = request.form['username']
        password = request.form['password']
        if username is '':
            return render_template('login.html.jinjia', userAlert = 1)
        elif password is '':
            return render_template('login.html.jinjia', passAlert = 1)
        else:
            user = User.query.filter_by(username = username).first()
            if user is None:
                return render_template('login.html.jinjia', userNo = 1)
            elif user.password != password:
                return render_template('login.html.jinjia', passNo = 1)
            else:
                session['username'] = username
                return redirect(url_for('index'))

    return render_template('login.html.jinjia')

@app.route('/logout')
def logout():
    session.clear()
    return render_template('index.html.jinjia')

@app.route('/create', methods=['GET', 'POST'])
def create():
    if request.method == 'POST':
        content = request.form['content']
        if content is '':
            return render_template('create.html.jinjia', conAlert = 1)
        else:
            user = User.query.filter_by(username = session['username']).first()
            post = Post(content = content, timestamp = datetime.now(), user_id = user.id)
            db.session.add(post)
            db.session.commit()
            return redirect(url_for('index'))
    return render_template('create.html.jinjia')

@app.errorhandler(404)
def page_not_found(error):
    return render_template('404.html.jinjia'), 404


app.run()
```
- create.py
``` python
import os

basedir = os.path.abspath(os.path.dirname(__file__))

SQLALCHEMY_DATABASE_URI = 'sqlite:///' + os.path.join(basedir, 'blog.db')
DEBUG = True
SECRET_KEY = 'myblog'
```
- index.html.jinjia
``` html
<html>
    <head>
        <title>Blog</title>
    </head>
    <body>
        {% if session.username %}
        <h1>Welcome to my blog, {{ session.username }}</h1>
        <p><a href="/signup">signup here</p>
        <p>you can create your blog <a href="/create">here</a>, and logout <a href="/logout">here</a></p>
        {% else %}
        <p><a href="/signup">signup here</p>
        <p><a href="/login">login here</p>
        {% endif %}
        <h1>Blog Content</h1>
        {% for blog in blogs %}
        <p> {{ blog.content }} {{ blog.timestamp }}</p>
        {% endfor %}
    </body>
</html>
```
- signup.html.jinjia
``` html
<html>
    <head>
        <title>Signup</title>
    </head>
    <body>
        <h1>Signup</h1>
        {% if userAlert %}
        <script>alert('Please input username');</script>
        {% endif %}
        {% if passAlert %}
        <script>alert('Please input password');</script>
        {% endif %}
        <form action="" method="post">
        <p>Uername: <input type = "txt" name = "username" ></p>
        <p>Password: <input type = "password" name = "password" ></p>
        <p><input type = "submit" name = "submit" value = "signup"></p>
        </form>
    </body>
</html>
```
- login.html.jinjia
``` python
<html>
    <head>
        <title>login</title>
    </head>
    <body>
        <form action="" method="post">
            <h1>Login</h1>
            {% if userAlert %}
            <script>alert('Please input username');</script>
            {% endif %}
            {% if passAlert %}
            <script>alert('Please input password');</script>
            {% endif %}
            {% if userNo %}
            <script>alert('Username is not exist');</script>
            {% endif %}
            {% if passNo %}
            <script>alert('Password is not incorrect');</script>
            {% endif %}
            <p>Uername: <input type = "txt" name = "username" ></p>
            <p>Password: <input type = "password" name = "password" ></p>
            <p><input type = "submit" name = "submit" value = "login"></p>
        </post>
    </body>
</html>
```
- create.html.jinjia
``` html
<html>
    <head>
        <title>Create</title>
    </head>
    <body>
        <h1>Create blog</h1>
        {% if conAlert %}
        <script>alert('Please input your content');</script>
        {% endif %}
        <form action="" method="post">
        <p>content: <input type = "txt" name = "content" ></p>
        <p><input type = "submit" name = "submit" value = "ok"></p>
        </form>
    </body>
</html>
```
