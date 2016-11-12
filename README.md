# homebridge-camera-ffmpeg

ffmpeg plugin for [Homebridge](https://github.com/nfarina/homebridge)

## Installation

1. Install ffmpeg on your Mac
2. Install this plugin using: npm install -g homebridge-camera-ffmpeg
3. Edit ``config.json`` and add the camera.
3. Run Homebridge
4. Add extra camera accessories in Home app. The setup code is the same as homebridge.

### Config.json Example

    {
      "platform": "Camera-ffmpeg",
      "cameras": [
        {
          "name": "Camera Name",
          "videoConfig": {
          	"source": "-re -i rtsp://myfancy_rtsp_stream",
            "stillImageSource": "-i http://faster_still_image_grab_url/this_is_optional.jpg"
          	"maxStreams": 2,
          	"maxWidth": 1280,
          	"maxHeight": 720,
          	"maxFPS": 30
          }
        }
      ]
    }

Incidentally, check [iSpyConnect's camera database](https://www.ispyconnect.com/sources.aspx) to find likely protocols and URLs to try with your camera.
