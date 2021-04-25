# Thumbor on Heroku
[![Deploy on Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/onurardal/thumbor-on-heroku.git)

[Thumbor](https://github.com/thumbor/thumbor) is a on-demand image manipulation service with cropping, resizing and filtering capabilities. When compared to other imaging libraries, the most important feature of thumbor is the smart cropping ([detectors](https://thumbor.readthedocs.io/en/latest/detectors.html)) feature which is uses machine learning ([cascade classification](https://docs.opencv.org/2.4.13.7/modules/objdetect/doc/cascade_classification.html)) for detection of important point on pictures.

# Example

Difference between normal and smart mode is the smart mode tries to protect focal points on picture. This difference can seen in the 2nd and 3rd picture. (*on 3rd picture, focal point is shifted towards the top rows players.*)

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

# Heroku Configuration

* [App Configuration](app.json)
    * Stack: heroku-16  
    heroku-16 used instead of heroku-18 because of the missing operating system packages (libpng, libjasper). [stack-configurations](https://devcenter.heroku.com/articles/stack-packages)
    * Buildpack: [heroku/python](https://github.com/heroku/heroku-buildpack-python)
* [Runtime](runtime.txt)
    * python-2.7.15
* [Pip Packages](requirements.txt)
    * thumbor
    * opencv-python-headless
* [Procfile](Procfile)
    * `web: thumbor -p $PORT`  
    Simply tells the thumbor which port should used.
