# SIP - Generation tool
To get this code to work you need to do the following steps: 
1. Install `darcs` a VCS like `git` or `svn`
`brew install darcs`

2. Fetch all repositories neede for python-sipsimple installation
[Sipsimple Installation Guide](http://sipsimpleclient.org/projects/sipsimpleclient/wiki/SipInstallation)
- This was what was needed on the 22/3-2017:
```
darcs get --set-scripts-executable http://devel.ag-projects.com/repositories/python-sipsimple
darcs get http://devel.ag-projects.com/repositories/python-xcaplib
darcs get http://devel.ag-projects.com/repositories/python-msrplib
darcs get http://devel.ag-projects.com/repositories/python-application
darcs get http://devel.ag-projects.com/repositories/python-application
darcs get http://devel.ag-projects.com/repositories/python-gnutls
darcs get http://devel.ag-projects.com/repositories/python-cjson
darcs get http://devel.ag-projects.com/repositories/python-eventlib
```
3. Install all dependencies plus some extra 
- Install the following python packages:
`pip install twisted zope.interface dnspython cython greenlet lxml python-dateutil python-cjson`
- To get `python-otr` working this should help:
```
brew install mpfr
brew install mpc
brew install libmpc

export LDFLAGS="-L/usr/local/opt/openssl/lib"
export CPPFLAGS="-I/usr/local/opt/openssl/include"
export PKG_CONFIG_PATH="/usr/local/opt/openssl/lib/pkgconfig"

pip install python-otr
```
### For more information:
[SIP Simple Client](http://sipsimpleclient.org/)