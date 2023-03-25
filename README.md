# Ansible rsyslog roles

Ansible roles to configure rsyslog for centralised logging. Tested on Redhat, Debian, and Ubuntu.

> I couldn't get the rsyslog version distributed with Ubuntu 22.04 to play nice as a central TLS (X509) destination so I install the version from ppa:adiscon/v8-stable.

Included for testing is a vagrant virtualbox setup. It uses my mkcert role: https://github.com/naebrae/ansible_mkcert to create a local CA signed certificate but any CA signed certificate can be used instead.

## Usage

```
vagrant up logsrv22 logcli22
./runansible x509.yml
```
