# snmptrapd-docker

Snmptrap server image.

Forked from [sig9org](https://github.com/sig9org/snmptrapd-docker) to:

1. Baseline Alpine and [Net-SNMP](http://www.net-snmp.org/) version in
   dockerfile.
2. Add `VOLUME` directives to `Docker` file to allow for persistant
   configuration files when image is used in
   [GNS3](https://github.com/GNS3/).

# Boot options

|Option|Description|
|-----|-----|
|-Lo|Log messages to the standard output stream.|
|-f|Do not fork() from the calling shell.|

# Usage

```sh
docker run -it --rm -p 162:162/udp --name snmptrapd karimkanso/snmptrapd
```

