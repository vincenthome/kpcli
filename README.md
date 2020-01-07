# Run keepass cli  (kpcli) under Docker Ubuntu with Network off to secure/prevent any outbound traffic.

## Repos

[GitHub: https://github.com/vincenthome/kpcli](https://github.com/vincenthome/kpcli)

[Docker Hub: https://hub.docker.com/r/vincenthome/kpcli](https://hub.docker.com/r/vincenthome/kpcli)


## Requirement: a file kp.kdbx in current folder. (kpcli has trouble using keyfile)

## Todo: 
* pass .kdbx filename as param
* try other kpcli command options
* fix ping which take 10 secs to return

## To run

1. Download docker-compose.yml
2. Run docker-compose and bind to current directory:

Mac/Linux 
```
docker-compose run -v ${PWD}:/data --rm kpcli 
```
Windows batch script
```
docker-compose run -v %cd%:/data --rm kpcli 
```

## kpcli Tutorial

* [kpcli](http://kpcli.sourceforge.net/)
* [https://www.digitalocean.com/community/tutorials/how-to-use-kpcli-to-manage-keepass2-password-files-on-an-ubuntu-14-04-server](https://www.digitalocean.com/community/tutorials/how-to-use-kpcli-to-manage-keepass2-password-files-on-an-ubuntu-14-04-server)
* [Best command-line Password Manager for Linux/ubuntu](https://www.techinfected.net/2016/05/kpcli-best-command-line-password-manager-ubuntu-linux-mint-debian.html)

## Troubleshoot using docker

```
docker run -it -v ~:/data vincenthome/kpcli
```

