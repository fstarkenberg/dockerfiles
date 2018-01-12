# SubtitleEdit
Container running [SubtitleEdit](http://www.nikse.dk/subtitleedit).
The container GUI is exposed via RDP and HTTP.

## Usage example:
`docker run --name=subtitleedit -e WIDTH=1280 -e HEIGHT=720 -p 3389:3389 -p 8080:8080 -v /media:/media fresta/subtitleedit`
