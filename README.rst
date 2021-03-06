============================
django-elasticsearch-dsl-drf
============================
Integrate `Elasticsearch DSL
<https://pypi.python.org/pypi/elasticsearch-dsl>`_ with
`Django REST framework <https://pypi.python.org/pypi/djangorestframework>`_ in
the shortest way possible, with least efforts possible.

Package provides views, serializers, filter backends, pagination and other
handy add-ons.

You are expected to use `django-elasticsearch-dsl
<https://pypi.python.org/pypi/django-elasticsearch-dsl>`_ for defining your
Elasticsearch documents.

Documentation
=============
Documentation is available on `Read the Docs
<http://django-elasticsearch-dsl-drf.readthedocs.io/>`_.

Make sure to read `FAQ <https://github.com/barseghyanartur/django-elasticsearch-dsl-drf/blob/master/docs/faq.rst>`_.

Prerequisites
=============
- Django 1.8, 1.9, 1.10, 1.11, 2.0, 2.1 and 2.2.
- Python 2.7, 3.5, 3.6, 3.7
- Elasticsearch 2.x, 5.x, 6.x

Main features and highlights
============================

- :doc:`Dynamic serializer for Documents <basic_usage_examples>`.
- :doc:`Search filter backend <advanced_usage_examples>`.
- :doc:`Ordering filter backend <advanced_usage_examples>`.
- :doc:`Filtering filter backend <advanced_usage_examples>` (big variety of
  native- and functional- query lookups, such as ``gt``, ``gte``, ``lt``,
  ``lte``, ``endswith``, ``contains``, ``wildcard``, ``exists``, ``exclude``,
  ``isnull``, ``range``, ``in``, ``prefix`` (same as ``startswith``), ``term``
  and ``terms`` is implemented.
- :doc:`Geo-spatial filtering filter backend <advanced_usage_examples>` (the
  following filters implemented: ``geo_distance``, ``geo_polygon`` and
  ``geo_bounding_box``).
- :doc:`Geo-spatial ordering filter backend <advanced_usage_examples>` (the
  following filters implemented: ``geo_distance``).
- :doc:`Faceted search filter backend <advanced_usage_examples>`.
- :doc:`Post-filter filter backend <advanced_usage_examples>`.
- :doc:`Nested filtering filter backend <nested_fields_usage_examples>`.
- :doc:`Highlight backend <advanced_usage_examples>`.
- :doc:`Suggester filter backend <advanced_usage_examples>`.
- :doc:`Functional suggester filter backend <advanced_usage_examples>`.
- :doc:`Pagination (Page number and limit/offset pagination) <advanced_usage_examples>`.
- :doc:`Ids filter backend <advanced_usage_examples>`.
- :doc:`Multi match search filter backend <search_backends>`.
- :doc:`Simple search query search filter backend <search_backends>`.
- :doc:`More-like-this support (detail action) <more_like_this>`.
- :doc:`Global aggregations support <global_aggregations>`.
- :doc:`Source filter backend <source_backend>`.

Demo
====
A frontend demo (React based) is available. See the `dedicated docs
<https://github.com/barseghyanartur/django-elasticsearch-dsl-drf/blob/master/examples/frontend/README.rst>`_
for more information.

To bootstrap evaluation, clone the repository locally and run `docker-compose`.

.. code-block:: sh

    docker-compose up

It will set up:

- Elasticsearch on `http://localhost:9200 <http://localhost:9200>`_
- Django REST framework on `http://localhost:8000 <http://localhost:8000>`_
- React on `http://localhost:3000 <http://localhost:3000>`_

Installation
============
(1) Install latest stable version from PyPI:

    .. code-block:: sh

        pip install django-elasticsearch-dsl-drf

    or latest stable version from GitHub:

    .. code-block:: sh

        pip install https://github.com/barseghyanartur/django-elasticsearch-dsl-drf/archive/stable.tar.gz

    or latest stable version from BitBucket:

    .. code-block:: sh

        pip install https://bitbucket.org/barseghyanartur/django-elasticsearch-dsl-drf/get/stable.tar.gz

(2) Add ``rest_framework``, ``django_elasticsearch_dsl`` and
    ``django_elasticsearch_dsl_drf`` to ``INSTALLED_APPS``:

    .. code-block:: python

        INSTALLED_APPS = (
            # ...
            # REST framework
            'rest_framework',

            # Django Elasticsearch integration
            'django_elasticsearch_dsl',

            # Django REST framework Elasticsearch integration (this package)
            'django_elasticsearch_dsl_drf',
            # ...
        )

Quick start
===========
Perhaps the easiest way to get acquainted with ``django-elasticsearch-dsl-drf``
is to read the :doc:`quick start tutorial <quick_start>`.

See it as a guide of diving into integration of Elasticsearch with Django
with very low knowledge entry level.

Testing
=======
Project is covered with tests.

To test with all supported Python/Django versions type:

.. code-block:: sh

    tox

To test against specific environment, type:

.. code-block:: sh

    tox -e py37-django21

To test just your working environment type:

.. code-block:: sh

    ./runtests.py

To run a single test in your working environment type:

.. code-block:: sh

    ./runtests.py src/django_elasticsearch_dsl_drf/tests/test_filtering.py

Or:

.. code-block:: sh

    ./manage.py test django_elasticsearch_dsl_drf.tests.test_ordering

To run a single test class in a given test module in your working environment
type:

.. code-block:: sh

    ./runtests.py src/django_elasticsearch_dsl_drf/tests/test_suggesters.py::TestSuggesters

It's assumed that you have all the requirements installed. If not, first
install the test requirements:

.. code-block:: sh

    pip install -r examples/requirements/test.txt

Writing documentation
=====================
Keep the following hierarchy.

.. code-block:: text

    =====
    title
    =====

    header
    ======

    sub-header
    ----------

    sub-sub-header
    ~~~~~~~~~~~~~~

    sub-sub-sub-header
    ^^^^^^^^^^^^^^^^^^

    sub-sub-sub-sub-header
    ++++++++++++++++++++++

    sub-sub-sub-sub-sub-header
    **************************

License
=======
GPL 2.0/LGPL 2.1

Support
=======
For any issues contact me at the e-mail given in the `Author`_ section.

Author
======
Artur Barseghyan <artur.barseghyan@gmail.com>
