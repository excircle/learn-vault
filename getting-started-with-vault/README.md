# Getting Started With HashiCorp Vault

This is a folder dedicated to the content found at: https://learn.hashicorp.com/collections/vault/getting-started


# Starting The Server

HashiCorp offers a tutorial on learning how to start a Vault server. The tutorial can be found at [Vault: Starting The Server](https://learn.hashicorp.com/tutorials/vault/getting-started-dev-server?in=vault/getting-started).

The begining of the tutorial has you start by initializing a "dev" server.

starting the dev server config output like the kind demonstrated below:

###Vault Startup Config

```bash
[akalaj@centos8-box ~]$ vault server -dev
==> Vault server configuration:

             Api Address: http://127.0.0.1:8200
                     Cgo: disabled
         Cluster Address: https://127.0.0.1:8201
              Go Version: go1.15.13
              Listener 1: tcp (addr: "127.0.0.1:8200", cluster address: "127.0.0.1:8201", max_request_duration: "1m30s", max_request_size: "33554432", tls: "disabled")
               Log Level: info
                   Mlock: supported: true, enabled: false
           Recovery Mode: false
                 Storage: inmem
                 Version: Vault v1.7.3
             Version Sha: 5d517c864c8f10385bf65627891bc7ef55f5e827

==> Vault server started! Log data will stream in below:
```

The values shown in the above example are as follows:

* `Api Address`:		The address where the API server is listening
* `Cgo`:				Cgo enables the creation of Go packages that call C code.
* `Cluster Address`:	The address where the cluster API server is listening
* `Go Version`:			The version of Go used to build the running version of Vault
* `Listener 1`:			Denotes "1" listener running, and what it's listening to
* `Log Level`:			Denotes how much debug information is being logged.
* `Mlock`:				Linux function allowing a process to lock a section of memory
* `Recovery Mode`:		Denotes if Vault is running in [Recovery Mode](https://www.vaultproject.io/docs/concepts/recovery-mode)
* `Storage`:			Specifies where Vault is storing data
* `Version`:			Version
* `Version Sha`:		The hash of the version

### Verification that the server is running successfully.

Once you have started the server, the below command demonstrates what a functional dev server status
should look like.

```bash

export AWS_ACCESS_KEY_ID=AKIAS3TCEFUXH4KHA64O; export AWS_SECRET_ACCESS_KEY=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