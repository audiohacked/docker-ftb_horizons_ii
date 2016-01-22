# Feed-The-Beast Horizons II (Minecraft 1.7.10) in a Docker Container
It's highly recommended to pull and run a data container:
```
docker pull audiohacked/minecraft_datastore
docker run --name ftb_horizons_datastore audiohacked/minecraft_datastore
```

Then, pull and run the server container:
```
docker pull audiohacked/ftb_horizons_ii
docker run -d --name ftb_horizons \
    --volumes-from ftb_horizons_datastore \
    -p 25565:25565 \
    -e EULA=TRUE \
    audiohacked/ftb_horizons_ii
```
