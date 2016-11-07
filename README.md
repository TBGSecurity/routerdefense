routerdefense
=============

Router Defense deep dives into Cisco router and switch configuration files and provides security recommendations.
It gives the opportunity to audit network devices in a quick, efficient way and provides actionable remediation actions.

The tool was originally released at the BRUCON 2010 conference and included around 140 tests.

It has been forked and now maintained by Ryan Hays at TBG Security.

# Requirements

Python 2.7

reportlab (pip install reportlab)

## Linux installation

```
git clone git@github.com:TBGSecurity/routerdefense.git

pip install reportlab
```

## Windows installation

```
Download & install http://www.python.org/ftp/python/2.7.5/python-2.7.5.msi

Downoload https://bitbucket.org/pypa/setuptools/raw/bootstrap/ez_setup.py

Execute c:\python27\python.exe ez_setup.py

Execute c:\python27\Scripts\easy_install.exe reportlab
```

## Help

```
./run_routerdefense -h
usage: run_routerdefense [-h] --iosconfig IOSCONFIG
                         [--iosplatform IOSPLATFORM] [--ip4inbound IP4INBOUND]
                         [--ip4outbound IP4OUTBOUND]
                         [--reportformat REPORTFORMAT]
                         [--reportfilename REPORTFILENAME]

Cisco IOS configuration security assessment tool.

optional arguments:
  -h, --help            show this help message and exit
  --iosconfig IOSCONFIG
                        Cisco IOS configuration file.
  --iosplatform IOSPLATFORM
                        Cisco IOS platform: router, switch or both (multiple
                        layers like Cat4k or 6k).
  --ip4inbound IP4INBOUND
                        Authorized nodes to do VTY inbound sessions (Telnet,
                        SSH). Possibles values examples (comma-separated) :
                        192.168.100.0/24, 192.168.1.1
  --ip4outbound IP4OUTBOUND
                        Authorized nodes to communicate with the device in the
                        outbound direction: SNMP, SYSLOG. Possibles values
                        examples (comma-separated) : 192.168.100.0/24,
                        192.168.1.1
  --reportformat REPORTFORMAT
                        Report format support: stdout, csv, html, pdf.
  --reportfilename REPORTFILENAME
                        Report filename.
```
