# windows-cpp-builder

## Setup:
#### docker for windows server
* mobyproject script
* fetch zip and copy to windows/system32

#### GitLab Runner Config

## Building
* `docker build . -t windows-cpp-builder:latest -m 4GB -c 6 --isolation=process`

