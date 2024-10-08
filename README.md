# synology-minecraft-bedrock

This is a Docker-based distribution of Bedrock Minecraft wrapped for deployment to Synology.

We essentially wrap Geoff Bourne's work at https://github.com/itzg/docker-minecraft-bedrock-server with slight changes to config.

New versions should release in Geoff's updates in docker, or any dependency updates.

# Build

```
bazel test //...
ls -al bazel-bin/spk/minecraft-bedrock/minecraft-bedrock.spk
-r-xr-xr-x  1 allanc  wheel  245760  2 Oct 10:33 bazel-bin/spk/minecraft-bedrock/minecraft-bedrock.spk
```

# Deploy

```
synopkg  install minecraft-bedrock.spk
```
## Check

```
sudo tail -f /var/log/synopkgmgr.log /var/log/synopkg.log
docker inspect bedrock-bedrock-1
```
