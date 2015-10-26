AsyncIO CRUD Store
==================

A very simple subset of databases capabilities intended to use most of them
the same way. You can use it to write database independent asyncio
libraries.

It currently supports mongodb (through [motor]) and postrgresql
(through [aiopg]), please feel free to add other dbs implementations.


Usage
-----
The api is very simple and obvious (I hope).
The working examples are in `examples` directory.

    # create
    id = await store.create({'foo': 'bar'})

    # read
    doc = await store.read(foo='bar')

    # update
    await store.update(id, {'foo': 'baz', 'spam': 1})

    # delete
    await store.delete(id)


[motor]: https://motor.readthedocs.org/
[aiopg]: https://aiopg.readthedocs.org/
