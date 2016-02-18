# proGres-cube


proGres-cube is an HTTP OLAP cube server for aggregation queries:
* Easy drilling-down
*  Slicing and dicing
* Serves aggregates, dimension details, facts
* Provides all necessary metadata for a reporting application


The repository contains configuration file for lightweight python file:

* [Cube Server](http://cubes.databrewery.org/) running on [http://localhost:5000](http://localhost:5000)
* [Cube Viewer](http://jjmontesl.github.io/cubesviewer/) running on [http://localhost:5000](http://localhost:5000)


This directory contains following files:

* model.json      - logical model
* slicer.ini      - server configuration file
* data.csv        - source data
* prepare_data.py - script for preparing the data: load them into database and create a view
* aggregate.py    - example aggregations
* 


## Installatio instruction

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

## Launch cube server
cd C:\cube\cubes-master\examples\hello_world

## Prepare data and run the OLAP server:
```python
python prepare_data.py
slicer serve slicer.ini
```


## Launch cube viewer
[Instruction](https://github.com/jjmontesl/cubesviewer/blob/master/doc/guide/cubesviewer-gui-installation.md)

cd C:\cube\cubesviewer-master\src\web\project

```python
python manage.py syncdb
```
