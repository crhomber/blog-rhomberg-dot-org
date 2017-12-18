Install a list of packets with yum
##################################
:date: 2011-05-21 12:34
:author: Christian
:tags: APT, aptitude, CentOS, Fedora, Linux, RedHat, RPM, YUM
:slug: install-a-list-of-packets-with-yum

Today I installed two new CentOS machines for a customer.

It was required to install exact the same packages on these boxes that
were installed on another system that was already in use.

I've never done this before and looked into the manpage of yum but was
not able to find a proper solutions there.

So I made it quick and dirty:

On the machine where you have everything installed:

    packets=\`rpm -qa\`
     echo $packets > packets.txt

Copy the packets.txt to the new machines.

On the new machines:

    packets=\`cat packets.txt\`
     yum install $packets
