# proGres-cube

proGres-cube is an HTTP OLAP cube server for aggregation queries:
* Easy drilling-down
*  Slicing and dicing
* Serves aggregates, dimension details, facts
* Provides all necessary metadata for a reporting application

The repository contains configuration file for lightweight python file:
* [Cube Server](http://cubes.databrewery.org/) running on [http://localhost:5000](http://localhost:5000)
* [Cube Viewer](http://jjmontesl.github.io/cubesviewer/) running on [http://localhost:8000](http://localhost:8000)


## Project Description

This directory contains following files:

* model.json      - logical model
* slicer.ini      - server configuration file
* data.csv        - source data
* prepare_data.py - script for preparing the data: load them into database and create a view
* aggregate.py    - example aggregations

## Installation instruction

You need to install [Python 2.7](https://www.python.org/downloads/)

Then you will need to get the following modules from Python. Open a CMD and run the command belows:

```python
pip install cubes[all]
pip install Django
pip install sqlalchemy
pip install flask
pip install flasker
pip install requests
pip install argparse
pip install djangorestframework
pip install wsgiref
```

You may also need to install the github client in order to donwload the app files from Github

## Cube server
Create a folder to host all the files -- Can be done in a cmd in Win.
```
cd C:\
mkdir cube
```

Get the files from Github - in Github shell
```
cd C:\cube
git clone git://github.com/DataBrewery/cubes.git
```

In a regular cmd, move to the folder where the cubes viewer files are
```
cd C:\cube\cubes\examples\hello_world
```

Then run the script to prepare data and run the OLAP server:

```python
python prepare_data.py
slicer serve slicer.ini
```


## Cubes viewer
See [Cubes Viewer Instruction](https://github.com/jjmontesl/cubesviewer/blob/master/doc/guide/cubesviewer-gui-installation.md)


Get the files from Github- in Github shell
```
cd C:\cube
git clone git://github.com/jjmontesl/cubesviewer.git
```

In a regular cmd, move to the folder where the cubes viewer files are
```
cd C:\cube\cubesviewer\src\web\project
```

Then run the script
```python
python manage.py syncdb
Python manage.py runserver
```
## ProGres Cube
Get the files from Github- in Github shell
```
cd C:\cube
git clone git://github.com/unhcr-mena/proGres-cube.git
```

Move to the folder where the cubes viewer files are
```
cd C:\cube\proGres-cube
```

