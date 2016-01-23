# Feed-The-Beast Horizons II (Minecraft 1.7.10) in a Docker Container
Pull image:
```
docker pull audiohacked/ftb_horizons_ii
```

It's highly recommended to run a data container:
```
docker run --name ftb_horizons_datastore audiohacked/ftb_horizons_ii true
```

Then, run the server container:
```
docker run -d --name ftb_horizons \
    --volumes-from ftb_horizons_datastore \
    -p 25565:25565 \
    -e EULA=TRUE \
    audiohacked/ftb_horizons_ii
```
