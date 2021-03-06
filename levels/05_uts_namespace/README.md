# Level 05: UTS namespace

The UTS namespace allows per container hostname. After moving to a new UTS namespace you can change the hostname without effecting the hostname of the machine.

Use the [sethostname()](https://rawgit.com/Fewbytes/rubber-docker/master/docs/linux/index.html#linux.sethostname) call provided by our `linux` module.

## How to check your work

Hostname within the container should be different from outside. Specifically, we want the hostname to be the container ID.

```
$ sudo python rd.py run -i ubuntu /bin/bash -- -c hostname
0c96ccc-ee60-11e5-b7ff-600308a39608
11196 exited with status 0
```
