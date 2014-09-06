This Docker image will build a minimal Fedora image using the
packages listed in the `packages` file.  It will place the finished
image in `/srv/fedora`, which you are expected to mount as a volume:

    docker run -v /var/tmp/fedora:/srv/fedora larsks/fedbuilder

You would end up with:

- `/var/tmp/fedora/fedora-docker.img` -- this is a tar file that you
  can import into docker with `docker import`.

- `/var/tmp/fedora/root` -- this is the unpacked root filesystem.

As of this writing, the finished image is approximately 150MB.

