# AngularBuildpack

To build with packeto buildpacks run the following command.

```bash
pack build angular-buildpack \
  --buildpack paketo-buildpacks/web-servers \
  --env BP_NODE_RUN_SCRIPTS=build \
  --env BP_WEB_SERVER=nginx \
  --env BP_WEB_SERVER_ROOT=dist/angular-buildpack \
  --builder paketobuildpacks/builder:base
```

To run the application container image run the following command:
```bash
docker run --rm -d --name angular-buildpacks --env PORT=8080 --publish 8080:8080 angular-buildpack
```
