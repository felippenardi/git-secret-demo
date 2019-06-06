## Git Secret Demo

# Getting access
The environment keys required to run the project are encrypted. In order to
decrypit and run the project, you'll need to follow these steps:

1. Install GPG Suite: https://gpgtools.org/
1. Generate a PGP key foryou
1. Ask someone with `git secret` access to [ include your PGP public key ]( http://git-secret.io/ )
1. Install `git secret`: http://git-secret.io/installation
1. Update your branch after they add your key with `git pull`
1. Reveal the secret files with `git-secret reveal`


# Giving Access

1. Add someone's PGP public key to the [GPG Suite App](https://gpgtools.org/)
1. Give them access to the secret files running `git add someone@youtrust.com` (email must match the one in the PGP public key)
1. Encrypt the files with `git-secret hide`
1. Commit and push the changes. From this commit on, this person will also be able to decrypt the secret files


# Adding a new file

1. Create your new secret file (or update the decrypted version of an existing one)
1. Make sure the decrypted secret file is ignored at `.gitignore`
1. Generate a encrypted version of this file with `git-secret hide`
1. Commit and push your changes. Now everyone listed in `git-secret whoknows` can decrypt it with `git-secret reveal` 
