# ImageCompressor
An image compressor in Python. This program uses the unsupervised K-means algorithm. The dockerized application is then deployed on a raspberry pi 4, an ege device.

In this project, I have shown that a normal image takes 4 seconds to upload while a compressed image takes 2 seconds. This shows that processing an image at edge takes less time thereby implementing low latency.

The container does the following things:
- Take an image file.
- Upload it to amazon S3.
- Compresses the image using unsupervised K-means.
- Upload the compressed image to amazon S3.
- To start the container, execute:

With docker-compose

```$ docker-compose up --build```

Without docker-compose

Unzip the project folder

Open the project folder

In linux

```cd PythonImageCompressor```

Build the docker image

```docker build -t imageproc .```

To run the container

```docker run imageproc```

Output

![output screen](output_screen.png?raw=true "Title")