nginx
=========

Install and configure Nginx with one virtual host

Requirements
------------

Requires **python-apt** to be installed

Role Variables
--------------

 - workers - Number of Nginx workers (grep processor /proc/cpuinfo | wc -l)
 - connections_per_worker - Max nuber of connection per one worker (ulimit -n)
 - cache - this option shows nginx what expire headers it should setup.
 - host - name of the virtual host domain
 - root - path to start folder in filesystem
 - template - jinja2 template of virtual host file. You should set it according your needs

Dependencies
------------

This role suggests of ansible (basic) role

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: webservers
      roles:
         - { role: nginx, host: "example.com", root: "/var/www", template: "default.j2" }

License
-------

Copyright (c) 2015 Vlad Byndych

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Author Information
------------------

If you have any questions please write me yojemail@gmail.com
