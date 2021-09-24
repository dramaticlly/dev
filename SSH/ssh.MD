## To check if github SSH key has been configured
```
$ ssh -T git@github.com

Hi dramaticlly! You've successfully authenticated, but GitHub does not provide shell access.
```

## to show current ssh key used
```
$ ssh-add -l -E md5

256 MD5:ba:e3:81:96:be:8c:11:58:7b:b8:c4:2e:31:0f:67:17 [+] touchid-mac (ECDSA)
```

## from memento
```
$ memento show --ssh

ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBGmCpqCwcEywRdSmyuEldn6lJ7M1E5FhLvnaR5jHuEVaAjnRdzO1NNSJqaPvqz8WrkfdP4OTMzeB9eqioAG3SXc= mac-C02F73SFMD6T:2916B858-C862-4103-8783-676177603CA1:stevezhang
```