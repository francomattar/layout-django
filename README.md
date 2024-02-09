{% comment %}

# Django Layout

`django-layout` provides sane defaults for new Django projects based on
[established best
practices](http://lincolnloop.com/django-best-practices/) and some
configuration setups frequently used in Lincoln Loop\'s projects, like
[using pip-tools for dependency
locking](https://lincolnloop.com/blog/python-dependency-locking-pip-tools/),
[using
setup.py](https://lincolnloop.com/blog/using-setuppy-your-django-project/)
and [making manage.py a console
script](https://lincolnloop.com/blog/goodbye-managepy/).

To use `django-layout`:

1.  follow the steps for Python installation from the
    [Pre-Requisites](#pre-requisites) section;

2.  create and activate a virtualenv:

        python3.9 -m venv .venv
        . .venv/bin/activate

3.  install Django with `pip install django`


*Note:  The text following this comment block will become the README.md of the new project.*

------------------------------------------------------------------------

{% endcomment %}

# {{ project_name }}

## Docker Installation

Build and run the project:

    docker-compose up --build

To run Django commands like migrations and shell or to enter the
container bash do:

    docker-compose run --rm app bash
    docker-compose run --rm app manage.py createsuperuser
    docker-compose run --rm app manage.py migrate
    docker-compose run --rm app manage.py shell

To stop containers run:

    docker-compose down

To update a container after adding a new requirement for example:

    docker-compose build

## Running the project

### Docker

Create super user:

    docker-compose run --rm app manage.py createsuperuser

Make sure you have the containers running:

    docker-compose up

Access [localhost:8000/{{ project_name }}/admin/](http://localhost:8000/{{ project_name }}/admin/).
