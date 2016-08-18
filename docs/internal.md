# Internal

Sequence:

```
seq {
  init;
  parallel {
    create;
	seq {
	  kernel-checkout;
	  kernel-build;
	}
	seq {
	  docker-checkout;
	  docker-build;
	}
  }
  kernel-install;
  docker-install;
  reboot;
}
```

Internally used parameters (Do NOT set manually):

 * `LDLK_INSTANCE`: instance name (e.g. "tmp01")
 * `LDLK_WORKDIR`:  work dir (e.g. "/tmp/ldlk")
 
 * `LDLK_KERNEL_GIT`: .. (e.g. "git://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git")
 * `LDLK_KERNEL_VERSION`: .. (e.g. "master", "v4.7")

 * `LDLK_DOCKER_GIT`: .. (e.g. "https://github.com/docker/docker.git")
 * `LDLK_DOCKER_VERSION`: .. (e.g. "master", "v1.12.0")
 
 * `LDLK_GCE_MACHINE_IMAGE`: image name (e.g. "https://www.googleapis.com/compute/v1/projects/ubuntu-os-cloud/global/images/ubuntu-1604-xenial-v20160815")
 * `LDLK_GCE_MACHINE_TYPE`:  machine type (e.g. "n1-standard-1")
