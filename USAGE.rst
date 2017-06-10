Usage
=====

language
********

- Spanish: 'es'
- USA, UK: 'en'
- México: 'mx'
- Argentina: 'ar'
- Chile: 'cl'
- Colombia: 'co'


- Example

.. code-block:: python

    import python_filmaffinity
    service = python_filmaffinity.Filmaffinity(lang='en')


search
******

+-----------+----------+--------+-----------------------------------+
| Parameter | Required |   Type | Description                       |
+===========+==========+========+===================================+
| title     |   False  | String | Search for the title of the movie |
+-----------+----------+--------+-----------------------------------+
| cast      |   False  | String | Search movies by actor            |
+-----------+----------+--------+-----------------------------------+
| director  |   False  | String | Search movies by the director     |
+-----------+----------+--------+-----------------------------------+
| from_year |   False  | String | Search start date                 |
+-----------+----------+--------+-----------------------------------+
| to_year   |   False  | String | Search end date                   |
+-----------+----------+--------+-----------------------------------+

- Example

.. code-block:: python

    movies = service.search(cast='Nicolas Cage')


get_movie
*********

+-----------+----------+--------+-----------------------------------+
| Parameter | Required |   Type | Description                       |
+===========+==========+========+===================================+
| id        |   False  | String | Filmaffinity id                   |
+-----------+----------+--------+-----------------------------------+
| title     |   False  | String | Get movie by title                |
+-----------+----------+--------+-----------------------------------+

- Example

.. code-block:: python

    movies = service.get_movie(title='Avatar')
    movies = service.get_movie(id='495280')


top_filmaffinity
****************

+-----------+----------+--------+-----------------------------------+
| Parameter | Required |   Type | Description                       |
+===========+==========+========+===================================+
| from_year |   False  | String | Search start date                 |
+-----------+----------+--------+-----------------------------------+
| to_year   |   False  | String | Search end date                   |
+-----------+----------+--------+-----------------------------------+
| top       |   False  | Integer| Number of elements                |
+-----------+----------+--------+-----------------------------------+

- Example

.. code-block:: python

    movies = service.top_filmaffinity()
    movies = service.top_filmaffinity(from_year=2010, to_year=2011)


top_premieres
*************

+-----------+----------+--------+-----------------------------------+
| Parameter | Required |   Type | Description                       |
+===========+==========+========+===================================+
| top       |   False  | Integer| Number of elements                |
+-----------+----------+--------+-----------------------------------+

- Example

.. code-block:: python

    movies = service.top_premieres()


top_netflix, top_hbo, top_filmin
********************************

+-----------+----------+--------+-----------------------------------+
| Parameter | Required |   Type | Description                       |
+===========+==========+========+===================================+
| top       |   False  | Integer| Number of elements                |
+-----------+----------+--------+-----------------------------------+

- Example

.. code-block:: python

    movies = service.top_netflix()
    movies = service.top_hbo(top=5)
    movies = service.top_filmin()


recommend HBO, Netflix, Filmin
******************************

+-----------+----------+--------+-----------------------------------+
| Parameter | Required |   Type | Description                       |
+===========+==========+========+===================================+
| top       |   False  | Integer| Number of elements                |
+-----------+----------+--------+-----------------------------------+

- Example

.. code-block:: python

    movies = service.recommend_netflix()
    movies = service.recommend_hbo()
    movies = service.recommend_filmin()