# CER generating for macOS

It seems many run into the issue of installing ***docker*** and have no Docker daemon after that.

```
$ docker ps
Cannot connect to the Docker daemon at unix:///var/run/docker.sock. Is the docker daemon running?
```

This can be caused by many issues, but to produce the error above, Docker was installed like this:

```bash
brew install Docker
```

To setup Docker on a mac, go to [Docker's website](https://docs.docker.com/docker-for-mac/install/) which explains how to use it.

Go to [Docker hub](https://hub.docker.com/editions/community/docker-ce-desktop-mac/) to get the community edition of Docker Desktop for Mac.

Ensure you download stable. Open the DMG, ignore any warnings, and drag Docker into programs. Then, go to 'Apps' and open Docker. It will now configure itself. Once this is completed, the whale in the menubar will show it's doing stuff by being animated, you can use Terminal to run Docker commands. Try `docker ps` again. If this works, run `./generate-pdf -d` enforcing the use of Docker to generate the pdf.

A popup will show, asking for permissions for Docker to write in the directory you're in. For this test, the repo was in `Documents` - so this is where it wants permissions for. Ignore any hesitation you have and grand the permission. Now, the pdf can be generated inside the container:

```
MBP-van-Martijn:test-mac mtenheuv$ ./generate-pdf
Generating pdf using docker...
Unable to find image 'quay.io/redhat-cop/ubi8-asciidoctor:v1.3' locally
v1.3: Pulling from redhat-cop/ubi8-asciidoctor
c4d668e2xxxx: Pull complete
ec1681b6xxxx: Pull complete
d0303343xxxx: Pull complete
3eefb58fxxxx: Pull complete
352966daxxxx: Pull complete
cdeebdd5xxxx: Pull complete
ee5ca262xxxx: Pull complete
Digest: sha256:0601710d91f4b8a20bdb0bf58c2c43924877e9900b963bf73408a4edecxxxxxx
Status: Downloaded newer image for quay.io/redhat-cop/ubi8-asciidoctor:v1.3
Generated: cer-mac-2020-09-23-11-20-40.pdf
```

The PDF is in the current directory and can be reviewed.

