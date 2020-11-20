# Installation
Installation Steps for Red Hat CRC

## Prerequisites 
Make sure you have the following:
* Red Hat account
* Log in to your redhat account: [Red Hat](https://cloud.redhat.com/openshift/install/crc/installer-provisioned)


## Installing CRC
Create a folder in your home dir

```
mkdir ~/crc
```

Open this folder

```
cd ~/crc
```

Download the CRC package

```
wget https://mirror.openshift.com/pub/openshift-v4/clients/crc/latest/crc-linux-amd64.tar.xz
```

Extract the tar
```
tar -xvf crc-linux-amd64.tar.xz
```

Move the binary file
```
sudo cp crc-linux-<version>-amd64/crc /usr/local/bin/crc
```

Clean your home dir
```
cd ~
rm -rf crc
```

## Test the installation
Run the following command and check if you get a respone:

```
crc version

# you should be getting something like this:
CodeReady Containers version: 1.18.0+bb304aa
OpenShift version: 4.6.1 (embedded in binary)
```


## Configuring CRC
