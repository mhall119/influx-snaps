# Influx Snaps

## Installing Snapcraft

### Ubuntu
```
snap install snapcraft
```

### Mac OSX
```
brew install snapcraft
```

### Other Linux

Find out how to install the Snapcraft snap on your distro at https://snapcraft.io/snapcraft


## Building the Snaps

### InfluxDB Server

```
cd influxdb
snapcraft snap
```

### InfluxDB CLI
```
cd influx
snapcraft snap
```

### Advanced build options

If you are having problems with `multipass` or want to avoid it, instead run:

```
snapcraft snap --provider=host --destructive-mode
```

The `--destructive-mode` is needed because this will build the snap on the local host rather than in a VM.


## Installing the Snaps

```
snap install influx*.snap --dangerous
```

The `--dangerous` is only needed because this is a local file that `snap` can't verify with the store.