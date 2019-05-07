# Thumbor on Heroku

[Thumbor](https://github.com/thumbor/thumbor) is a on-demand image manipulation service with cropping, resizing and filtering capabilities. When compared to other imaging libraries, the most important feature of thumbor is the smart cropping ([detectors](https://thumbor.readthedocs.io/en/latest/detectors.html)) feature.

[![Deploy on Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/metinirden/thumbor-on-heroku)

This example covers http_module, face_detector and feature_detector.

<figure align="center">
  <img src="https://raw.githubusercontent.com/metinirden/thumbor-on-heroku/master/tottenham-example.jpg"/>
  <figcaption><small>Orginal Image (w:1886 h:1227)</small></figcaption>
</figure>
<br/>
<figure align="center">
  <img src="https://thumbor-on-heroku.herokuapp.com/unsafe/1200x400/https://raw.githubusercontent.com/metinirden/thumbor-on-heroku/master/tottenham-example.jpg"/>
  <figcaption><small>Cropped Image (w:1200 h:400)</small></figcaption>
</figure>
<br/>
<figure align="center">
  <img src="https://thumbor-on-heroku.herokuapp.com/unsafe/1200x400/smart/https://raw.githubusercontent.com/metinirden/thumbor-on-heroku/master/tottenham-example.jpg"/>
  <figcaption><small>Smart Cropped Image (w:1200 h:400)</small></figcaption>
</figure>
