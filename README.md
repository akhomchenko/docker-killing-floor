Killing Floor server
===

### How to build

> NOTE: Killing Floor server requires login to download server, so `login anonymous` is not going to work.

```bash
docker build -t gagoman/killing-floor --build-arg username=... --build-arg password=... --build-arg code=... .
```

Replace `...` with actual values, where `code` is 2FA. In case you do not have 2FA enabled just skip setting the 
parameter.

### How to run

```bash
docker run --rm -it -p 0.0.0.0:7707:7707/udp -p 0.0.0.0:7708:7708/udp -p 0.0.0.0:7717:7717/udp -p 0.0.0.0:28852:28852/udp -p 0.0.0.0:8075:8075/tcp -p 0.0.0.0:20560:20560/udp gagoman/killing-floor
```
