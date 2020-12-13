# 283assignment3
Step 1: Get kernel sources from GitHub link https://github.com/torvalds/linux/blob/master/arch/x86/kvm/cpuid.c

Step 2: modify cupid.c ,add c funtions to test cpuid ox4FFFFFFF.

Step 3: Run the following command on terminal • sudo bash • apt-get install build-essential kernel-package fakeroot libncurses5-dev libssl-dev ccache bison flex libelf-dev • sudo make -j 1 && sudo make modules_install -j 1 && sudo make install -j 1 • reboot • sudo rmmod arch/x86/kvm/kvm-intel.ko • sudo rmmod arch/x86/kvm/kvm.ko • sudo insmod arch/x86/kvm/kvm.ko • sudo insmod arch/x86/kvm/kvm-intel.ko

Step 4: install KVM and packages, then install virt-manager and CPUID(0x4FFFFFFE), exit number 1 exits=321. • sudo apt-get install qemu-kvm libvirt-bin bridge-utils virt-manager • sudo apt-get install virt-manager • sudo apt-get install cupid


Comment on the frequency of exits – does the number of exits increase at a stable rate? Or are there more exits performed during certain VM operations? Approximately how many exits does a full VM boot entail?

The number of the exits does not increase at a stable rate. There are more exits performed during certain operations.

Of the exit types defined in the SDM, which are the most frequent? Least?
Basic exit reason 2.Triple fault is the most frequent. 	changes to descriptor tables and control registers are the least.

