# Multi-stage Docker file template for serving (demo) DL model
This is templates for build a demo DL (typical in flask or fastApi).

In most of case, just copy `Dockerfile` to the `root folder` and build.

Some case, some modifies are need:
- beside libraries in requirements.txt, some or the dependency should install by apt-get

## Build and use
To build and use
    
    cd $ROOT_FOLDER
    docker build -t $IMAGE_NAME .
    
Run test, e.g., Flask with port 5000.
    
    docker run --rm -p 5000:5000 $IMAGE_NAME
    
## tips

For serving without GPU, can install pytorch CPU version with and extra index in begin of the requiremnts.txt file as below

    --extra-index-url https://download.pytorch.org/whl/cpu

`apt-get install -y --no-install-recommends` is typical used in case you need install some dependency.
