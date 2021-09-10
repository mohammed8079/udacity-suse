## Setup k3s

1. Install k3s following the instructions from [k3s website](https://k3s.io/)
2. We need to have admin right to run kubectl commands. Run `sudo su -`
3. We might encounter the following error with some versions of k3s: `Error: failed to create containerd container: get apparmor_parser version: exec: "apparmor_parser": executable file not found in $PATH`. Run `zypper install apparmor-parser` command to remove the error. A glitch here writing apparmor_parser instead of apparmor-parser.