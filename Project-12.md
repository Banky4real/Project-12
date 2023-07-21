## **Documentation for Project 12**

### Refactoring our Ansible for better maintainablity and extensibility

### Creating a new directory for jenkins to save artifacts to reduce complexity

`sudo mkdir /home/ubuntu/ansible-config-artifact`

![ansible-config-artifacts-directory-created](./Images/ansible-config-artifacts-directory-created.png)

### Permission changed for jenkins to save artifacts in the new directory

`chmod -R 0777 /home/ubuntu/ansible-config-artifact`

![permission-changed-for-jenkins-to-save-artifacts](./Images/permission-changed-for-jenkins-to-save-artifacts.png)

### Copy Artifact plugin Installed on Jenkins

![copy-artifact-plugin-installed](./Images/copy-artifact-plugin-installed-without-restart.png)

### save_artifact freestyle project created on Jenkins

![Save-artifact-freestyle-project-created](./Images/Save-artifact-freestyle-project-created.png)

### Configuring Number of Builds to Keep and which Project to Build Artifacts from

![Build-Config-Settings](./Images/configuring-number-of-builds-to-keep-and-which-project-to-trigger-build-from.png)

### Configuring a Build Step to copy artifact from project11ansible and Specifying the target directory which is ansible-config-artifact

![configuring-build-step](./Images/configuring-build-step-to-copy-artifact-from-another-project.png)

### Successfully-configured
![copy-artifact-successfully-configured](./Images/copy-artifact-successfully-configured.png)

### Testing our setup by making changes to readme file
![tested-with-changes-made-to-readme-file](./Images/tested-with-changes-made-to-readme-file-and-build-successful.png)

### Details of save_artifact first build in Console Output
![console-output](./Images/console-output-for-save_artifact-first-build.png)

### Our Jenkins Pipeline Looking neat, and Less Complex
![Less-Complex-jenkins-pipeline](./Images/Less-Complex-jenkins-pipeline.png)

## Refactoring Ansible by Importing Playbooks for different tasks

### This is achieved by having a parent playbook named site.yml which will be used as a refference point for other playbooks (Child Playbooks)

### Our Folder structure after having our parent playbook and child playbooks

![Folder-structure-for-our-playbook-imports](./Images/folder-structure-for-ansible-config-mgt.png)

### Running our Parent playbook site.yml against our dev environment for the removal(deleting) of wireshark, making use of the built-in ansible import-playbook Module and refferencing the child playbook static-assignment/common-del.yml
` ---`
` - hosts: all `
` - import_playbook: ../static-assignments/ ` `common-del.yml `

` ansible-playbook -i inventory/dev.yml playbooks/site.yml `
![running-ansible-playbook-import-against-dev-environment](./Images/running-ansible-playbook-import-against-dev-environment-for-deleting-wireshark.png)

### Confirmation of removal(deleting) wireshark on all our target servers

![wireshark-removal-confirmation-on-all-servers](./Images/wireshark-removal-confirmation-on-all-servers.png)