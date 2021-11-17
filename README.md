# Magma-with-bazel

Git clone magma repo
```bash
https://github.com/magma/magma.git
```
Set Env - vim /etc/environment 
```bash
MAGMA_ROOT=path to your magma clone
```
Build magma-builder base image
```bash
docker-compose build magma-builder
```
Exec into a magma-builder container ,to run bazel commands 
```bash
docker-compose run magma-builder bash
```
Once insider the container, bazel can be run like this
```bash
# To build all targets
bazel build ...
# To build a specific target (Ex: session_manager.proto)
bazel build lte/protos:session_manager_cpp_proto
# To run all tests
bazel test ...
```
