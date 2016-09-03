# docker-golang-gtk

Docker image to play with golang and gtk, it is based on [golang
wheezy](https://hub.docker.com/_/golang/)

### Versions

- **golang:** 1.7
- **gtk:** 2.0

### Running in MacosX


#### Install

1. Install xquartz `brew cask install xquartz`
2. Install socat `brew install socat`

#### Running

1. Start xquartz `open -a XQuartz`
2. Start socat `socat TCP-LISTEN:6000,reuseaddr,fork UNIX-CLIENT:\"$DISPLAY\"`
3. Start docker image `docker run -e DISPLAY=192.168.1.105:0 -ti --rm -v "$PWD":/usr/src/myapp
   -w /usr/src/myapp krolow/golang-gtk /bin/bash`

Replace `192.168.1.105` by your ip, afterwards when you build and run the app it will display
in Xquartz.

## License

Licensed under [The MIT License](http://krolow.mit-license.org/)
Redistributions of files must retain the above copyright notice.

## Author

Vinícius Krolow - krolow[at]gmail.com

