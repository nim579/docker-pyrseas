# docker-pyrseas
Pyrseas tool docker image.

Pyrseas provides a framework and utilities to upgrade and maintain a relational database — http://pyrseas.projects.pgfoundry.org/

## Create a `Dockerfile`

```
FROM nim579/pyrseas

ADD ./schema.yml ./schema.yml

CMD yamltodb --update $PGDATABASE schema.yml
```

## Running

```
docker run -e PGHOST=localhost -e PGPORT=5432 -e PGUSER=postgres -e PGPASSWORD=password -e PGDATABASE=mydatabase pyrseas
```

## Pyrseas docs

http://pyrseas.readthedocs.io/en/latest/index.html
