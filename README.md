# yocto-docker
A Dockerfie for Yocto project building.

In order to run firstly build docker image using:
```
git clone https://github.com/ivysochyn/yocto-docker
cd yocto-docker
sudo docker build -t yoctobuilder .
```

Once image is build, you can use it for yocto-project building whenever you want to just by running:
```
cd <yocto-project-dir>
sudo docker run --rm -v $PWD:/data -u $(id -u):$(id -u) -it yoctobuilder
```
