### Python Face Detection

This is a tiny script that uses opencv to detect different faces in an image.

It outputs the type of object detected, the boundary box that surrounds the object and the confidence level.

This can form the basis of detecting if an image has a clear face of a person e.g a profile picture.

As an example, you can reject any image with a confidence level lower than 0.9 and with more than one person.

## Getting the environment ready

Install Anaconda for managing the python environment:
```
https://www.anaconda.com/distribution/
```

Create a new python environment (Preferably the latest python):
```
conda create -n gundua python=3.11.0
```

Activate the environment:
```
condo activate gundua
```

Install tensorflow and opencv (This step can hang sometimes. If it does use conda search and specify the exact version when installing):
```
conda install tensorflow opencv
```

Install cvlib:
```
pip install cvlib
```

Run the script:
```
python detect.py
```

N.B

For mac, I've found that the anaconda environment might at times not work too well. You would have to install tensorflow and opencv through pip3 to make it work properly:

```
pip3 install opencv-python
pip3 install tensorflow
```

Then run with python3 instead of just python:

```
python3 detect.py
```

Remember edit the dev.local.exs to point to python3 instead of just python:
```
config :gundua, Gundua.Worker,
  python: "/Users/thomasjgx/anaconda3/bin/python3",
  detect_script: "/Users/thomasjgx/Research/face_detection/detect.py"
```