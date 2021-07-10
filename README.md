# Docker-Images

These are docker images exposed by Kiba Labs for generic purposes.

## App-Serve

This image is intended to make serving a react app extremely simple. To use, just create a dockerfile with the following:

```
FROM node:XYZ as build
... build you app ...

FROM ghcr.io/kibalabs/app-serve:latest
COPY --from=build /app/dist /usr/share/nginx/html
```

This image is intended to be used with https://github.com/kibalabs/build-js (although it's not required), so it will create a `runtimeConfig.js` file with all the environment variables available to the runtime (i.e. when `docker run` is executed) that begin with `KRT_`. These can then be accessed in your application as `window.KRT_`.
