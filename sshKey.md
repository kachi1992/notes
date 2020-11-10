##1. generate keys locally which can be used repeatedly
```
ssh-keygen -t rsa
```

public key:~/.ssh/id_rsa.pub
private key:~/.ssh/id_rsa

##2. write public key in server
```
touch .ssh/authorized_keys
chmod 700 .ssh
chmod 600 .ssh/authorized_keys
cat id_rsa.pub >> .ssh/authorized_keys
```

##3. config locally
```
vi ~/.ssh/config
```
```
Host hostAbbr
  HostName hostIP
  User userName
  IdentityFile ~/.ssh/id_rsa
```

```
ssh hostAbbr
```

