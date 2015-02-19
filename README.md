ansible-lockdown
----------------

### Intro

This is intended to serve a centralized repo utilizing submodules that point to STIG and CIS repositories. Each individual STIG and CIS repo is intended to be available via Ansible Galaxy.

### Instructions

This repository is meant to serve as the hub for all STIG and CIS work maintained and vetted by Ansible and our Security partner MindPointGroup

The different baseline repos are easily available via Ansible Galaxy; of course cloning  is also ok.


### STIGS

The standards are pulled directly from [DISA]. 


### CIS 

The standards are pulled directly from [CIS].


### Contributing

Contributions to ansible-lockdown will follow a similar process to the main Ansible project. Fork the repository, make changes, and submit a pull-request. Pull-request should not contain any merges or merge-conflicts.

Feature request, bug reports, etc, should all be opened as GitHub tickets. An ansible-lockdown mailing list is in the works.


Current Build Statuses For STIGS*
--------------------------------

|    OS    |     Repo     |         Status          | 
| ---------|--------------|--------------------------
| RedHat 6 |   [Repo][0]  | ![STATUS][rhel6status]  |

**Note:** A green badge represents a successful build which consists of:
  1. Creating an AWS EC2 instance from the AMI's provided by AWS as defaults.
  2. Applying the STIG baselines as available in the repository.
  3. Using [OpenSCAP][openscap] and [STIGMA][stigma-repo] to further validate the application of the baselines.
  4. Repeats the above for each profile: MAC-1 Public through MAC-3 Classified



[0]:https://github.com/nousdefions/ansible-role-stig
[rhel6status]:https://codeship.com/projects/6ff25160-95b3-0132-d4fc-466960a0e7d2/status?branch=devel
[DISA]:http://iase.disa.mil/stigs/Pages/index.aspx
[CIS]:https://benchmarks.cisecurity.org
[stigma-repo]:https://github.com/defionscode/STIGMA
[openscap]:http://www.open-scap.org/page/Main_Page
