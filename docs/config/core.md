# Core

This page documents the core configuration of Zipline.

## `CORE_RETURN_HTTPS`

Whether or not to return an `https` url.

<Alert type="danger">
You will need to set this to true, if using [SSL](/docs/config/ssl).
</Alert>

```bash
CORE_HTTPS=true
```

## `CORE_SECRET`

The secret key used to sign sensitive data. IF the value remains as `changethis` then Zipline will exit with an error telling you to change it.

```bash
CORE_SECRET=changethis
```

## `CORE_HOST`

The hostname to listen on. Keep as `0.0.0.0` if using docker, usually `0.0.0.0` will work in other cases not using docker.

```bash
CORE_HOST=0.0.0.0
```

## `CORE_PORT`

The port to listen on.

```bash
CORE_PORT=3000
```

## `CORE_DATABASE_URL`

The PostgreSQL database url.

```bash
CORE_DATABASE_URL=postgres://user:password@host:port/database
```

## `CORE_STATS_INTERVAL`

The number of seconds to wait until refreshing statistics of Zipline. This is used to reduce load times when viewing statistics on the dashboard.

```bash
CORE_STATS_INTERVAL=1800
```

## `CORE_COMPRESSION_ENABLED`

Whether to have compression enabled. This is used to save on bandwidth by enabling the `?compress` query in the `/r/:id` and the `/u/:id` endpoints. Currently, this is experimental and could end up compressing contents that should\'t be compressed. This is disabled by default.

```bash
CORE_COMPRESSION_ENABLED=true
```

## `CORE_COMPRESSION_THRESHOLD`

The amount of bytes a file size can be before it can be compressed. For more info on what values are accepted, see [here](/docs/guides/byte-format). The default, if enabled, is 2048 bytes.

```bash
CORE_COMPRESSION_THRESHOLD=1gb
```

## `CORE_COMPRESSION_ON_DASHBOARD`

Whether to have compression be used on the dashboard. This will have all images on the dashboard, excluding built in, be served with compression in mind.

```bash
CORE_COMPRESSION_ON_DASHBOARD=true
```