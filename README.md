# Kameleon Big Data Analytics

Kameleon recipe for an HPC Big Data Analytics software stack
based on a Debian 9 (Stretch) template.

Basic content:

- Oracle's java
- Apache Hadoop
- Apache Spark
- Apache Flink
- Apache HBase
- Apache Cassandra
- Apache Thrift
- ZeroMQ
- OpenMPI

Kameleon is a software appliance builder: http://kameleon.imag.fr

Backend used to build the image from recipes: qemu

**Watch out!**
Binary files in this repo are stored using Git Large File Storage (LFS)
Execute `git-lfs checkout` to get them.


## Accessing image

Root's password: kameleon

Additionally, a user is created during the image creation process
(user/password: kameleon). By commenting this line in the base.yaml
recipe (default/from_upstream_build/base.yaml), this user is available
in the final image:

       #  Uncomment the following line in base.yaml to clear user'kameleon'
       #  in the final image:
       #  - clean_system


## Testing image in a computer with QEMU

Launch with QEMU in your local system

       qemu-system-x86_64 -enable-kvm build/myvebida_stretch/myvebida_stretch.qcow2
