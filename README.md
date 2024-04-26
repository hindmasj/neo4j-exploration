# An Exploration Of Neo4j

See [Neo4j Home](https://neo4j.com/).

I have been wanting to have a proper play with this for a while, so here is some notes on how I am progressing.

## Install Docker Instance

See [Neo4j On Docker](https://neo4j.com/docs/operations-manual/current/docker/introduction/).

Here I am using a ".env" file to set the version of the image to pull and the sub-type of a RedHat UBI9 base distro. This file also sets a default password for the "neo4j" user when logging in. A volume is created by default at "${HOME}/volumes/neo4j". Make sure this directory exists before starting the instance. Note that this volume ends up being owned by the Neo4j internal user, which as a UID of 7474.

Created a docker compose YAML file so to start the image just ``docker compose up -d``.

Connect to the GUI by going to http://localhost:7474/browser. When there select username and password "neo4j/password" (or whatever you have set "NEO4J_AUTH to) and click "Connect". Try out the 3 guides that are presented.

Access a shell from the command line with ``docker compose exec neo4j bin/cypher-shell``. You need to supply the same username and passowrd as above.

