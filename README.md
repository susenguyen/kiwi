# Kiwi build for SL Micro 6.1
- requires https://geeko2.suse.lab as RMT
- kiwi 10 (used from a Tumbleweed VM)
- kiwi file + config script from https://build.opensuse.org/package/show/SUSE:Templates:Images:SL-Micro-6.1/SL-Micro

# Modifications
- Set the repository to https://geeko2.suse.lab

# Building the VM
- openSUSE Tumbleweed minimal
- Packages
    - python3-kiwi
    - qemu-img 
    - gptfdisk 
    - kpartx 
    - e2fsprogs 
    - squashfs 
    - xorriso

# Running kiwi-ng
- Set the TARGET_DIR to whatever directory you want to save your images to
```
kiwi-ng --profile=x86-self_install --type=oem system build --description=desc --target-dir=${TARGET_DIR}
```
