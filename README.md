# Thumbor on Heroku

[Thumbor](https://github.com/thumbor/thumbor) is a on-demand image manipulation service with cropping, resizing and filtering capabilities. When compared to other imaging libraries, the most important feature of thumbor is the smart cropping ([detectors](https://thumbor.readthedocs.io/en/latest/detectors.html)) feature which is uses machine learning ([cascade classification](https://docs.opencv.org/2.4.13.7/modules/objdetect/doc/cascade_classification.html)) for detection of important point on pictures.

[![Deploy on Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/metinirden/thumbor-on-heroku)


><p align="center">
>    <img src="tottenham-example.jpg"/>
>    <em>Orginal Image (w:1886 h:1227)</em>
>  <br/>
>  <br/>
>    <img src="https://thumbor-on-heroku.herokuapp.com/unsafe/1200x400/https://raw.githubusercontent.com/metinirden/thumbor-on-heroku/master/tottenham-example.jpg"/>
>    <em>Cropped Image (w:1200 h:400)</em>
>  <br/>
>  <br/>
>    <img src="https://thumbor-on-heroku.herokuapp.com/unsafe/1200x400/smart/https://raw.githubusercontent.com/metinirden/thumbor-on-heroku/master/tottenham-example.jpg"/>
>    <em>Smart Cropped Image (w:1200 h:400 )</em>
></p>