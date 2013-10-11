## aws-swap-init

aws-swap-init is a chkconfig and LSB-capable init script which can be used to automatically create a swapfile on an EC2 instance if one does not already exist. It supports Ubuntu and RedHat-derivative OSes. If ephemeral disk is present, it will create the swapfile there. If not, or if the OS is an unsupported type, it will use /.

### Installation

Simply install in `/etc/init.d`. Then:

#### Ubuntu
````
update-rc.d aws-swap-init defaults
````

#### RedHat derivatives
````
chkconfig --add aws-swap-init
chkconfig aws-swap-init on
````

### License

Copyright 2012 Corsis
http://www.corsis.com/

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
