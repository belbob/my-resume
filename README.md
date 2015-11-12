# Create "my-resume" for devs or production

## Start by cloning the repo:
```sh
git clone git@github.com:belbob/my-resume.git
```

## Vagrant: my-resume for developing use

### run the vm
```sh
cd my-resume/vagrant/
vagrant up
```
### get IP-address
```sh
vagrant ssh-config
```
view "my-resume" in your browser at "ip.add.ress"


## Docker: my-resume in production

### Build the image
```sh
cd my-resume/docker/
docker build -t="robert/my-resume" .
```
### Run the container
```sh
docker run -d -p 8888:80 robert/my-resume
```
view "my-resume" in your browser at "localhost:8888"
