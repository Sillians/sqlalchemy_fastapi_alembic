# sqlalchemy_fastapi_alembic
A simple guide / implementation on how to utilize fastapi with relational databases and the use of alembic for database migrations.



### pipenv
Pipenv: Python Development Workflow for Humans

`Pipenv` is a tool that aims to bring the best of all packaging worlds (bundler, composer, npm, cargo, yarn, etc.) to the Python world.

It automatically creates and manages a virtualenv for your projects, as well as adds/removes packages from your Pipfile as you install/uninstall packages. It also generates the ever-important `Pipfile.lock`, which is used to produce deterministic builds.
 - sudo apt install pipenv


#### creating pipenv environment for python 3
 - $ pipenv --three (Deprecated, uses python3 by default)
 - $ pipenv --python 3.7

- activating the pipenv environment
 - $ pipenv shell

#### if you have multiple python 3 versions installed then
 - $ pipenv install -d --python 3.10.4

- install all dependencies (include -d for installing dev dependencies)
 - $ pipenv install -d


### Docker compose file
The docker compose configuration will create a cluster with 3 containers

- web container — where the actual code will run
- postgres-db container
- pgadmin container


### Alembic
Let initialize `Alembic` by running the following command in the terminal;
- `alembic init migration`
- This will create a directory called `migration` and 
    - config file `alembic.ini` , We set the sqlalchemy.url to point to our database.
    - The `env.py` is a Python script that performas a lot of the heavy lifting
    - `script.py.mako` is a template for generating migration scripts.
    - The `versions` directory is where our migration scripts go.


### create a .env file
Add the following
- `DATABASE_URL = postgresql+psycopg2://{user}:{password}@{host}:{port}`
indicating the following;
    - `user`
    - `password`
    - `host`
    - `port`




