# PDM Plone 6 setup, including 2 ZEO clients

This setup is meant to use with [PDM](https://pdm.fming.dev).

## Setup

### Install dependencies

To install all dependencies, run the following command.

```shell
pdm install
```

### Create ZEO server config

To create a ZEO Server configuration, run this command.

```shell
pdm run zeo_create
```

### Create ZEO client configs

To create configurations for ZEO clients, run the following command with a instanceXX.yml file as parameter.
By default we have two instance configurations, but you can create more.

```shell
pdm run client_create instance01.yml
pdm run client_create instance02.yml
```

Now we have a ZEO Server config and two ZEO clients.

## Running Plone

### Starting the ZEO server

```shell
pdm run zeo_start
```

### Starting the ZEO Clients

Start client1

```shell
pdm run client1_start
```

in another shell run

```shell
pdm run client2_start
```

both clients run in foreground.
For production, we can use supervisor or Systemd scripts.
