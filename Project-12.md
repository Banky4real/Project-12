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