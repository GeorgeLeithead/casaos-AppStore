# CasaOS - AppStore
A personal and customised App store for CasaOs and the ZimaBoard, to include what I personally wanted and needed, especially for .NET development.

## Original Source
This is originally from the source of [CasaOS AppStore](https://github.com/IceWhaleTech/CasaOS-AppStore)

## LinuxServer AppStore
The containers are based on the Linux images from [LinuxServer.io](https://www.linuxserver.io/) images.

## How to install
This is only supported on CasaOS version [0.4.4] and above.

Run the following command to install the appstore:
```bash
casaos-cli app-management register app-store https://<path to build release ZIP file>/<ZIP file name>.zip
```

### Apps
In addition to the standard CasaOS apps, these are the additional container apps added:


### Troublshooting


### Error 404 Not Found when running the install command

This could be cause by your CasaOS running on a port other than the default `port 80`. You need to add the `-u` flag at the end to tell command which port your CasaOS is running:

```bash
casaos-cli app-management register app-store https://<path to build release ZIP file>/<ZIP file name>.zip -u "localhost:<my-casa-os-port>"
```

Replace `<my-casa-os-port>` with the port where your CasaOS is running. For example if my CasaOS is running on port 90:

```bash
casaos-cli app-management register app-store https://<path to build release ZIP file>/<ZIP file name>.zip -u "localhost:90"
```
