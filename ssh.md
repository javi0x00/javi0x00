# :memo: Notes
## SSH
- - -
### Resources
* [OpenSSH](https://www.openssh.com/manual.html)
* [GitHub with SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)
* [GitLab with SSH](https://docs.gitlab.com/ee/ssh/)
* [Bitbucket with SSH](https://support.atlassian.com/bitbucket-cloud/docs/set-up-an-ssh-key/)
* [PuTTY](https://www.putty.org/)
### Terms and concepts
* SSH
* SSH server
* SSH client
* Private key
* Public key
#### Basic commands
Install
```
$ apt-get install openssh-server
$ systemclt enable ssh
$ 
```
Connect
```
$ ssh <user>@<ip>
$ .ssh/authorized_keys
```
Key
```
$ ssh-keygen
$ eval $(ssh-agent)
$ ssh-add
$ ssh-add -D
```
Tests
```
$ ssh -T git@github.com
$ ssh -T git@gitlab.com
$ ssh -T git@bitbucket.org
```
- - -
## Software Developer
[Javier Andrés Garzón Patarroyo](https://javierandres.dev)
