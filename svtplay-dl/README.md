# svtplay-dl
Container running [svtplay-dl](https://github.com/spaam/svtplay-dl).
* Built on alpine.
* Should include all requirements, including ffmpeg, rtmpdump and pycrypto.
* `svtplay-dl` is the entrypoint.

## Usage example:
`docker run -it --rm -v "$(pwd):/data" fresta/svtplay-dl`

Or create an alias in `~/.bash_aliases`:  
`alias svtplay-dl='docker run -it --rm -v "$(pwd):/data" fresta/svtplay-dl'`

## Build example:
`docker build --build-arg VERSION=1.9.6 -t svtplay-dl:1.9.6 .`
