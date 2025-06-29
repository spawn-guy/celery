.. image:: https://docs.celeryq.dev/en/latest/_images/celery-banner-small.png

|build-status| |coverage| |license| |wheel| |semgrep| |pyversion| |pyimp| |ocbackerbadge| |ocsponsorbadge|

:Version: 5.5.3 (immunity)
:Web: https://docs.celeryq.dev/en/stable/index.html
:Download: https://pypi.org/project/celery/
:Source: https://github.com/celery/celery/
:DeepWiki: |deepwiki|
:Keywords: task, queue, job, async, rabbitmq, amqp, redis,
  python, distributed, actors

Donations
=========

Open Collective
---------------

.. image:: https://opencollective.com/static/images/opencollectivelogo-footer-n.svg
   :alt: Open Collective logo
   :width: 200px

`Open Collective <https://opencollective.com/celery>`_ is our community-powered funding platform that fuels Celery's
ongoing development. Your sponsorship directly supports improvements, maintenance, and innovative features that keep
Celery robust and reliable.

For enterprise
==============

Available as part of the Tidelift Subscription.

The maintainers of ``celery`` and thousands of other packages are working with Tidelift to deliver commercial support and maintenance for the open source dependencies you use to build your applications. Save time, reduce risk, and improve code health, while paying the maintainers of the exact dependencies you use. `Learn more. <https://tidelift.com/subscription/pkg/pypi-celery?utm_source=pypi-celery&utm_medium=referral&utm_campaign=enterprise&utm_term=repo>`_

Sponsors
========

Blacksmith
----------

.. image:: ./docs/images/blacksmith-logo-white-on-black.svg
   :alt: Blacksmith logo
   :width: 240px
   :target: https://blacksmith.sh/

`Official Announcement <https://www.linkedin.com/pulse/celery-now-powered-blacksmith-tomer-nosrati-ew68e/?trackingId=DWHH49WqS2iOW8Jf5N1kEg%3D%3D>`_

CloudAMQP
---------

.. image:: ./docs/images/cloudamqp-logo-lightbg.svg
   :alt: CloudAMQP logo
   :width: 240px
   :target: https://www.cloudamqp.com/

`CloudAMQP <https://www.cloudamqp.com/>`_ is a industry leading RabbitMQ as a service provider.
If you need highly available message queues, a perfect choice would be to use CloudAMQP.
With 24,000+ running instances, CloudAMQP is the leading hosting provider of RabbitMQ,
with customers all over the world.

Upstash
-------

.. image:: https://upstash.com/logo/upstash-dark-bg.svg
   :alt: Upstash logo
   :width: 200px
   :target: https://upstash.com/?code=celery

`Upstash <http://upstash.com/?code=celery>`_ offers a serverless Redis database service,
providing a seamless solution for Celery users looking to leverage
serverless architectures. Upstash's serverless Redis service is designed
with an eventual consistency model and durable storage, facilitated
through a multi-tier storage architecture.

Dragonfly
---------

.. image:: https://github.com/celery/celery/raw/main/docs/images/dragonfly.svg
   :alt: Dragonfly logo
   :width: 150px
   :target: https://www.dragonflydb.io/

`Dragonfly <https://www.dragonflydb.io/>`_ is a drop-in Redis replacement that cuts costs and boosts performance.
Designed to fully utilize the power of modern cloud hardware and deliver on the data demands of modern applications,
Dragonfly frees developers from the limits of traditional in-memory data stores.



.. |oc-sponsor-1| image:: https://opencollective.com/celery/sponsor/0/avatar.svg
    :target: https://opencollective.com/celery/sponsor/0/website

What's a Task Queue?
====================

Task queues are used as a mechanism to distribute work across threads or
machines.

A task queue's input is a unit of work, called a task, dedicated worker
processes then constantly monitor the queue for new work to perform.

Celery communicates via messages, usually using a broker
to mediate between clients and workers. To initiate a task a client puts a
message on the queue, the broker then delivers the message to a worker.

A Celery system can consist of multiple workers and brokers, giving way
to high availability and horizontal scaling.

Celery is written in Python, but the protocol can be implemented in any
language. In addition to Python there's node-celery_ for Node.js,
a `PHP client`_, `gocelery`_, gopher-celery_ for Go, and rusty-celery_ for Rust.

Language interoperability can also be achieved by using webhooks
in such a way that the client enqueues an URL to be requested by a worker.

.. _node-celery: https://github.com/mher/node-celery
.. _`PHP client`: https://github.com/gjedeer/celery-php
.. _`gocelery`: https://github.com/gocelery/gocelery
.. _gopher-celery: https://github.com/marselester/gopher-celery
.. _rusty-celery: https://github.com/rusty-celery/rusty-celery

What do I need?
===============

Celery version 5.5.x runs on:

- Python (3.8, 3.9, 3.10, 3.11, 3.12, 3.13)
- PyPy3.9+ (v7.3.12+)


This is the version of celery which will support Python 3.8 or newer.

If you're running an older version of Python, you need to be running
an older version of Celery:

- Python 3.7: Celery 5.2 or earlier.
- Python 3.6: Celery 5.1 or earlier.
- Python 2.7: Celery 4.x series.
- Python 2.6: Celery series 3.1 or earlier.
- Python 2.5: Celery series 3.0 or earlier.
- Python 2.4: Celery series 2.2 or earlier.

Celery is a project with minimal funding,
so we don't support Microsoft Windows but it should be working.
Please don't open any issues related to that platform.

*Celery* is usually used with a message broker to send and receive messages.
The RabbitMQ, Redis transports are feature complete,
but there's also experimental support for a myriad of other solutions, including
using SQLite for local development.

*Celery* can run on a single machine, on multiple machines, or even
across datacenters.

Get Started
===========

If this is the first time you're trying to use Celery, or you're
new to Celery v5.5.x coming from previous versions then you should read our
getting started tutorials:

- `First steps with Celery`_

    Tutorial teaching you the bare minimum needed to get started with Celery.

- `Next steps`_

    A more complete overview, showing more features.

.. _`First steps with Celery`:
    https://docs.celeryq.dev/en/stable/getting-started/first-steps-with-celery.html

.. _`Next steps`:
    https://docs.celeryq.dev/en/stable/getting-started/next-steps.html

 You can also get started with Celery by using a hosted broker transport CloudAMQP. The largest hosting provider of RabbitMQ is a proud sponsor of Celery.

Celery is...
=============

- **Simple**

    Celery is easy to use and maintain, and does *not need configuration files*.

    It has an active, friendly community you can talk to for support,
    like at our `mailing-list`_, or the IRC channel.

    Here's one of the simplest applications you can make:

    .. code-block:: python

        from celery import Celery

        app = Celery('hello', broker='amqp://guest@localhost//')

        @app.task
        def hello():
            return 'hello world'

- **Highly Available**

    Workers and clients will automatically retry in the event
    of connection loss or failure, and some brokers support
    HA in way of *Primary/Primary* or *Primary/Replica* replication.

- **Fast**

    A single Celery process can process millions of tasks a minute,
    with sub-millisecond round-trip latency (using RabbitMQ,
    py-librabbitmq, and optimized settings).

- **Flexible**

    Almost every part of *Celery* can be extended or used on its own,
    Custom pool implementations, serializers, compression schemes, logging,
    schedulers, consumers, producers, broker transports, and much more.

It supports...
================

    - **Message Transports**

        - RabbitMQ_, Redis_, Amazon SQS, Google Pub/Sub

    - **Concurrency**

        - Prefork, Eventlet_, gevent_, single threaded (``solo``)

    - **Result Stores**

        - AMQP, Redis
        - memcached
        - SQLAlchemy, Django ORM
        - Apache Cassandra, IronCache, Elasticsearch
        - Google Cloud Storage

    - **Serialization**

        - *pickle*, *json*, *yaml*, *msgpack*.
        - *zlib*, *bzip2* compression.
        - Cryptographic message signing.

.. _`Eventlet`: http://eventlet.net/
.. _`gevent`: http://gevent.org/

.. _RabbitMQ: https://rabbitmq.com
.. _Redis: https://redis.io
.. _SQLAlchemy: http://sqlalchemy.org

Framework Integration
=====================

Celery is easy to integrate with web frameworks, some of which even have
integration packages:

    +--------------------+------------------------+
    | `Django`_          | not needed             |
    +--------------------+------------------------+
    | `Pyramid`_         | `pyramid_celery`_      |
    +--------------------+------------------------+
    | `Pylons`_          | `celery-pylons`_       |
    +--------------------+------------------------+
    | `Flask`_           | not needed             |
    +--------------------+------------------------+
    | `web2py`_          | `web2py-celery`_       |
    +--------------------+------------------------+
    | `Tornado`_         | `tornado-celery`_      |
    +--------------------+------------------------+
    | `FastAPI`_         | not needed             |
    +--------------------+------------------------+

The integration packages aren't strictly necessary, but they can make
development easier, and sometimes they add important hooks like closing
database connections at ``fork``.

.. _`Django`: https://djangoproject.com/
.. _`Pylons`: http://pylonsproject.org/
.. _`Flask`: https://flask.palletsprojects.com/
.. _`web2py`: http://web2py.com/
.. _`Bottle`: https://bottlepy.org/
.. _`Pyramid`: https://docs.pylonsproject.org/projects/pyramid/en/latest/
.. _`pyramid_celery`: https://pypi.org/project/pyramid_celery/
.. _`celery-pylons`: https://pypi.org/project/celery-pylons/
.. _`web2py-celery`: https://code.google.com/p/web2py-celery/
.. _`Tornado`: https://www.tornadoweb.org/
.. _`tornado-celery`: https://github.com/mher/tornado-celery/
.. _`FastAPI`: https://fastapi.tiangolo.com/

.. _celery-documentation:

Documentation
=============

The `latest documentation`_ is hosted at Read The Docs, containing user guides,
tutorials, and an API reference.

.. _`latest documentation`: https://docs.celeryq.dev/en/latest/

.. _celery-installation:

Installation
============

You can install Celery either via the Python Package Index (PyPI)
or from source.

To install using ``pip``:

::


    $ pip install -U Celery

.. _bundles:

Bundles
-------

Celery also defines a group of bundles that can be used
to install Celery and the dependencies for a given feature.

You can specify these in your requirements or on the ``pip``
command-line by using brackets. Multiple bundles can be specified by
separating them by commas.

::


    $ pip install "celery[redis]"

    $ pip install "celery[redis,auth,msgpack]"

The following bundles are available:

Serializers
~~~~~~~~~~~

:``celery[auth]``:
    for using the ``auth`` security serializer.

:``celery[msgpack]``:
    for using the msgpack serializer.

:``celery[yaml]``:
    for using the yaml serializer.

Concurrency
~~~~~~~~~~~

:``celery[eventlet]``:
    for using the ``eventlet`` pool.

:``celery[gevent]``:
    for using the ``gevent`` pool.

Transports and Backends
~~~~~~~~~~~~~~~~~~~~~~~

:``celery[amqp]``:
    for using the RabbitMQ amqp python library.

:``celery[redis]``:
    for using Redis as a message transport or as a result backend.

:``celery[sqs]``:
    for using Amazon SQS as a message transport.

:``celery[tblib``]:
    for using the ``task_remote_tracebacks`` feature.

:``celery[memcache]``:
    for using Memcached as a result backend (using ``pylibmc``)

:``celery[pymemcache]``:
    for using Memcached as a result backend (pure-Python implementation).

:``celery[cassandra]``:
    for using Apache Cassandra/Astra DB as a result backend with the DataStax driver.

:``celery[azureblockblob]``:
    for using Azure Storage as a result backend (using ``azure-storage``)

:``celery[s3]``:
    for using S3 Storage as a result backend.

:``celery[gcs]``:
    for using Google Cloud Storage as a result backend.

:``celery[couchbase]``:
    for using Couchbase as a result backend.

:``celery[arangodb]``:
    for using ArangoDB as a result backend.

:``celery[elasticsearch]``:
    for using Elasticsearch as a result backend.

:``celery[riak]``:
    for using Riak as a result backend.

:``celery[cosmosdbsql]``:
    for using Azure Cosmos DB as a result backend (using ``pydocumentdb``)

:``celery[zookeeper]``:
    for using Zookeeper as a message transport.

:``celery[sqlalchemy]``:
    for using SQLAlchemy as a result backend (*supported*).

:``celery[pyro]``:
    for using the Pyro4 message transport (*experimental*).

:``celery[slmq]``:
    for using the SoftLayer Message Queue transport (*experimental*).

:``celery[consul]``:
    for using the Consul.io Key/Value store as a message transport or result backend (*experimental*).

:``celery[django]``:
    specifies the lowest version possible for Django support.

    You should probably not use this in your requirements, it's here
    for informational purposes only.

:``celery[gcpubsub]``:
    for using Google Pub/Sub as a message transport.



.. _celery-installing-from-source:

Downloading and installing from source
--------------------------------------

Download the latest version of Celery from PyPI:

https://pypi.org/project/celery/

You can install it by doing the following:

::


    $ tar xvfz celery-0.0.0.tar.gz
    $ cd celery-0.0.0
    $ python setup.py build
    # python setup.py install

The last command must be executed as a privileged user if
you aren't currently using a virtualenv.

.. _celery-installing-from-git:

Using the development version
-----------------------------

With pip
~~~~~~~~

The Celery development version also requires the development
versions of ``kombu``, ``amqp``, ``billiard``, and ``vine``.

You can install the latest snapshot of these using the following
pip commands:

::


    $ pip install https://github.com/celery/celery/zipball/main#egg=celery
    $ pip install https://github.com/celery/billiard/zipball/main#egg=billiard
    $ pip install https://github.com/celery/py-amqp/zipball/main#egg=amqp
    $ pip install https://github.com/celery/kombu/zipball/main#egg=kombu
    $ pip install https://github.com/celery/vine/zipball/main#egg=vine

With git
~~~~~~~~

Please see the Contributing section.

.. _getting-help:

Getting Help
============

.. _mailing-list:

Mailing list
------------

For discussions about the usage, development, and future of Celery,
please join the `celery-users`_ mailing list.

.. _`celery-users`: https://groups.google.com/group/celery-users/

.. _irc-channel:

IRC
---

Come chat with us on IRC. The **#celery** channel is located at the
`Libera Chat`_ network.

.. _`Libera Chat`: https://libera.chat/

.. _bug-tracker:

Bug tracker
===========

If you have any suggestions, bug reports, or annoyances please report them
to our issue tracker at https://github.com/celery/celery/issues/

.. _wiki:

Wiki
====

https://github.com/celery/celery/wiki

Credits
=======

.. _contributing-short:

Contributors
------------

This project exists thanks to all the people who contribute. Development of
`celery` happens at GitHub: https://github.com/celery/celery

You're highly encouraged to participate in the development
of `celery`. If you don't like GitHub (for some reason) you're welcome
to send regular patches.

Be sure to also read the `Contributing to Celery`_ section in the
documentation.

.. _`Contributing to Celery`:
    https://docs.celeryq.dev/en/stable/contributing.html

|oc-contributors|

.. |oc-contributors| image:: https://opencollective.com/celery/contributors.svg?width=890&button=false
    :target: https://github.com/celery/celery/graphs/contributors

Backers
-------

Thank you to all our backers! 🙏 [`Become a backer`_]

.. _`Become a backer`: https://opencollective.com/celery#backer

|oc-backers|

.. |oc-backers| image:: https://opencollective.com/celery/backers.svg?width=890
    :target: https://opencollective.com/celery#backers

.. _license:

License
=======

This software is licensed under the `New BSD License`. See the ``LICENSE``
file in the top distribution directory for the full license text.

.. # vim: syntax=rst expandtab tabstop=4 shiftwidth=4 shiftround

.. |build-status| image:: https://github.com/celery/celery/actions/workflows/python-package.yml/badge.svg
    :alt: Build status
    :target: https://github.com/celery/celery/actions/workflows/python-package.yml

.. |coverage| image:: https://codecov.io/github/celery/celery/coverage.svg?branch=main
    :target: https://codecov.io/github/celery/celery?branch=main

.. |license| image:: https://img.shields.io/pypi/l/celery.svg
    :alt: BSD License
    :target: https://opensource.org/licenses/BSD-3-Clause

.. |wheel| image:: https://img.shields.io/pypi/wheel/celery.svg
    :alt: Celery can be installed via wheel
    :target: https://pypi.org/project/celery/

.. |semgrep| image:: https://img.shields.io/badge/semgrep-security-green.svg
    :alt: Semgrep security
    :target: https://go.semgrep.dev/home

.. |pyversion| image:: https://img.shields.io/pypi/pyversions/celery.svg
    :alt: Supported Python versions.
    :target: https://pypi.org/project/celery/

.. |pyimp| image:: https://img.shields.io/pypi/implementation/celery.svg
    :alt: Supported Python implementations.
    :target: https://pypi.org/project/celery/

.. |ocbackerbadge| image:: https://opencollective.com/celery/backers/badge.svg
    :alt: Backers on Open Collective
    :target: #backers

.. |ocsponsorbadge| image:: https://opencollective.com/celery/sponsors/badge.svg
    :alt: Sponsors on Open Collective
    :target: #sponsors

.. |downloads| image:: https://pepy.tech/badge/celery
    :alt: Downloads
    :target: https://pepy.tech/project/celery

.. |deepwiki| image:: https://devin.ai/assets/deepwiki-badge.png
    :alt: Ask http://DeepWiki.com
    :target: https://deepwiki.com/celery/celery
    :width: 125px
