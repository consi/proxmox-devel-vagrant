proxmox-devel-vagrant
=====================
An Vagrantfile for Proxmox Virtual Environment (PVE) development

Usage
-----
Just clone this repository and invoke command (this assumes that you have vagrant installed and configured):
```
vagrant up
```

And then You can access development VM by typing:
```
vagrant ssh
```

Cloned directory is shared to /vagrant inside VM

Purpose
-------
This way You can easily dive in into Proxmox VE development to build patches for community. Also ansible used with this Vagrant can be used with bare metal host to make deployment of proxmox development machines easier

Limitations
-----------
You cannot test VMs inside Vagrant as VirtualBox doesn't support nested virtualization ; Main purpose of this Vagrant setup is to provide quick way to work mostly on API and Frontend components.
Most needed submodules are in proxmox-modules


License
-------
The MIT License (MIT)

Copyright (c) 2017 Marek Wajdzik

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
