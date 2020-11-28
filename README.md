# Trivial Secret Sharing

https://en.wikipedia.org/wiki/Secret_sharing#Trivial_secret_sharing

Split:
```
$ ./tss 5 <<< some-secret-key
RW3USqLP23HqhDjjqKnj
UQLfyCV183r99X8Rw/zr
NeDLjX+8wTqk7P4TtPjj
0fNgI2Gms6hgRoYn+49n
gxPNSbTTP/qhvkvrT0f1
```

Join:
```
$ ./tss <<EOT
> RW3USqLP23HqhDjjqKnj
> UQLfyCV183r99X8Rw/zr
> NeDLjX+8wTqk7P4TtPjj
> 0fNgI2Gms6hgRoYn+49n
> gxPNSbTTP/qhvkvrT0f1
> EOT
some-secret-key
```

Test:
```
$ echo my-data | ./tss 100 | ./tss
my-data
```
