# mitmproxy docker images

This docker image sets up a mitmproxy which does SSL description.

CA data is stored in the `/ca` volume which should be mounted somewhere persistent if you don't like adding a new certificate each time.

The port `8080` should be mapped to allow remote connections to the proxy server.

    docker run -t -i -p 8080:8080 \
               -v ~/.mitmproxy:/ca \
               tandrup/mitmproxy
