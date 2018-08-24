Run TiddlyWiki 5 via docker.


## Quickstart

    sudo docker run -d -p 8080:8080 hjlhust/tiddlywiki

Now TiddlyWiki should be running on [http://localhost:8080](http://localhost:8080).

## Keeping the data

The container uses a Docker volume to save the wiki data. In order not
to lose sight of that, I recommend using a local folder for the volume.

    sudo docker run -d -p 8080:8080 -v $(pwd)/.tiddlywiki:/var/lib/tiddlywiki hjlhust/tiddlywiki

In this example, the folder `$(pwd)/.tiddlywiki` is used for the data.

# Auth

Default auth is `hujl` / `wiki`

Simply provide the USERNAME and PASSWORD env variables to customise.

# Other settings

If you are in a memory-constrained environment, you can provide the
`NODE_MEM` environment variable to specify the memory ceiling (in MB)
