# Jenkins CI Cluster

Role for installing Jenkins Farm with agents via Docker-Compose

## Requirements

Required docker installation and/or docker role.

## Role Variables

- `jenkins_agent_1_secret`: Secret for connecting to the main cluster for agent 1.
- `jenkins_agent_2_secret`: Secret for connecting to the main cluster for agent 2.
- `jenkins_archive_password`: Password for the Jenkins home archive tarball.
- `jenkins_package_version`: Version of the Jenkins package to be installed.
- `Jenkins_Docker_root`: Root folder required for Jenkins Docker farm.

## Dependencies

Use this template infrastructure under galaxy.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:


```yaml
- hosts: Jenkins-CI
  gather_facts: yes
  become: yes
  roles:
    - role: Jenkins-Cluster
      vars:
        jenkins_agent_1_secret: "AGENT_1_SECRET"
        jenkins_agent_2_secret: "AGENT_2_SECRET"
        jenkins_archive_password: "ARCHIVE_PASSWORD"
        jenkins_package_version: "1.2.0"
        Jenkins_Docker_root: "/opt/jenkins"
        
```

In this example, the playbook is targeting the hosts under the "Jenkins-CI" group. Facts are gathered, and privilege escalation (become) is enabled. The Jenkins-Cluster role is applied with the provided variables, customizing its behavior during execution. The variables `jenkins_agent_1_secret`, `jenkins_agent_2_secret`, `jenkins_archive_password`, `jenkins_package_version`, and `Jenkins_Docker_root` are set to their respective values. Please make sure to adjust the inventory group and any other variables as per your specific setup.

## License

BSD