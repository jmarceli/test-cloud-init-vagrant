# test-cloud-init-vagrant

Create `.env` file with the following content:

```
VAGRANT_EXPERIMENTAL="cloud_init,disks"
```

Modify `cloud-init-test.yml` file and then execute `vagrant up`.
Test your VM with `vagrant ssh` to see the results of your cloud-init execution.

For more details please check https://www.grzegorowski.com/how-to-test-cloud-init-locally-with-vagrant

---

author: Jan Grzegorowski
