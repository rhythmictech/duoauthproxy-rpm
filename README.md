# duoauthproxy-rpm
RPM spec for Duo authentication proxy

Currently only tested with CentOS 6.

Build steps with mock look something like:

```
mock -r epel-6-x86_64 --init
spectool -g -R SPECS/duoauthproxy.spec
mock -r epel-6-x86_64 --buildsrpm --spec=SPECS/duoauthproxy.spec --sources=SOURCES --resultdir=SRPMS 
mock -r epel-6-x86_64 --no-clean --sources=SOURCES --resultdir=RPMS SRPMS/duoauthproxy-2.10.1-1.el6.src.rpm
```
