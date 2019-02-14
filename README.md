# GoGoBgp 
---
This is a gobgp container that can be used to run goBgp within your docker environment. It is 21 MB in size! Leveraging scratch allows it to be lean for usage. 

# Running It With config

`docker run -d --rm --name go-bgp -v $(pwd):/gobgp -p 179:179 -t yaml -f bgpConfig.yml`

# Adding A Route To Play With The API
`docker exec go-bgp /go/bin/gobgp global rib add -a ipv4 1.1.1.1/32`