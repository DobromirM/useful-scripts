Verify signature:
`gpg --verify <file.sig> <file>`

Verify checksum: 
`sha1sum -c <file.sha>`

Encrypt file:
`gpg -c <file>`

Decrypt file:
`gpg -d <file.gpg>`

Import key:
`gpg --import <file.gpg>`

Key permissions:
`chmod 600 <key>`

Renewing keys:

1) Import master key.

2) Edit key:
`gpg --expert --edit-key $MKEYID`

3) Select keys:
```
gpg> key 1
gpg> key 2
gpg> key 3
```
4) Change expiration:
`gpg> expire`

5) Save:
`gpg> save`

6) Export new public key:
`gpg --armor --export $KEYID > gpg-$KEYID-pub.asc`

Import SSH key:
1) `cd ~/.ssh`
2) `ssh-keygen -K`
3) Rename to `id_ecdsa_sk` and `id_ecdsa_sk.pub`

Note:
Check interfaces with yubikey manager to make sure that usb FIDO2 is enabled.
