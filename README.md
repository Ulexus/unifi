# Ubiquiti UniFi server

Ubiquiti's UniFi server, based on [`jasonrm/docker-unifi`](https://github.com/jasonrm/docker-unifi).

It expects to find a volume in `/var/lib/unifi/`, where it will store all state.  To be at all useful, you will need to expose the service ports, as well. 

See the [example unit file](/unifi.service) or try something like:

```
  docker run --rm --name unifi -v /data/unifi:/var/lib/unifi -p 8080:8080 -p 8091:8091 -p 8843:8843 -p 8880:8880 -p 8443:8443 -p 5353:5353/udp ulexus/unifi
```
