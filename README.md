# Docker Wordpress

Image to run Wordpress in docker

## Quick reference

### Build the image

```
docker build -t davidetriso/wordpress:[tagname-dir_name] ./[tagname-dir_name]
```

E.g.:

```
docker build -t davidetriso/wordpress:php-8.1-fpm ./php-8.1-fpm
```

### Push image to Docker Hub

```
docker push davidetriso/wordpress:tagname
```

E.g.:

```
docker push davidetriso/wordpress:php-8.1-fpm
```

###  Build and push everything

Execute the `./build-and-push.sh` script to build and push all images to Docker Hub at once.


## How to use

//TODO

The image uses a production-optimized php.ini file. To customize the PHP settings to your needs it is sufficient to bind-mount a custom ini file in the container's `/usr/local/etc/php/conf.d/` directory.

E.g.:

```yaml
wordpress:
    # ... other settings here ...
    volumes:
        # ... other volumes and mounts here ...
        - ./my/custom/999-php.ini:/usr/local/etc/php/conf.d/999-php.ini:ro
```

## License

Licensed under the terms of the [MIT](LICENSE) license.