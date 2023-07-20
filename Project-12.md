## **Documentation for Project 12**

### Refactoring our Ansible for better maintainablity and extensibility

### Creating a new directory for jenkins to save artifacts to reduce complexity

`sudo mkdir /home/ubuntu/ansible-config-artifact`

![ansible-config-artifacts-directory-created](./Images/ansible-config-artifacts-directory-created.png)

### Permission changed for jenkins to save artifacts in the new directory

`chmod -R 0777 /home/ubuntu/ansible-config-artifact`

![permission-changed-for-jenkins-to-save-artifacts](./Images/permission-changed-for-jenkins-to-save-artifacts.png)