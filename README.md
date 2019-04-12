## [fastlane match](https://docs.fastlane.tools/actions/match/)

This repository contains all your certificates and provisioning profiles needed to build and sign your applications. They are encrypted using OpenSSL via a passphrase.

**Important:** Make sure this repository is set to private and only your team members have access to this repo.

Do not modify this file, as it gets overwritten every time you run _match_.

### Installation

Make sure you have the latest version of the Xcode command line tools installed:

```
xcode-select --install
```

Install _fastlane_ using

```
[sudo] gem install fastlane -NV
```

or alternatively using `brew cask install fastlane`

### Usage

Navigate to your project folder and run

```
fastlane match appstore
```
```
fastlane match adhoc
```
```
fastlane match development
```
```
fastlane match enterprise
```

For more information open [fastlane match git repo](https://docs.fastlane.tools/actions/match/)

### 手动加密、解密
```
#加密 
openssl aes-256-cbc -k "passphrase" -in "distribution.cer" -out "jiami_distribution.cer" -a -e 

#解密 
openssl aes-256-cbc -k "passphrase" -in "CNW4VUR734.cer" -out "distribution.cer" -a -d 

```
- [reference:Fastlane 证书管道里（二）](https://juejin.im/post/5b1f1cf6f265da6e0b7004a8)

### Content

#### certs

This directory contains all your certificates with their private keys

#### profiles

This directory contains all provisioning profiles

------------------------------------

For more information open [fastlane match git repo](https://docs.fastlane.tools/actions/match/)
