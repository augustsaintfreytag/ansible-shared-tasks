This project is a repertoir of playbooks, task and other definitions used with the [Ansible](https://www.ansible.com/resources/get-started) automation framework. Tasks defined here can be imported as a Git Submodule and reused across projects with similar requirements in their build and deployment methodologies. The central usage scenario assumed by the authors is developing a web application locally and publishing to a virtual private server or cloud server instance. The configuration was put together for use with DigitalOcean, though it should function with other Linux-based servers, as well.

## Variables

Some tasks may use certain variables to control what kind of operations they perform through other utilities or what data is used for specific operations. Included task definitions with specific variable requirements are listed in this section.

### Certificate Provisioning

Creating certificates uses the publicly available service [Let's Encrypt](https://letsencrypt.org). When including the task, the following variables should be defined, as well.

#### `server_certificate_root`
The root directory all output and dependency files for `certbot` are placed for permanent residence on the server, commonly set to `/etc/letsencrypt`.

#### `server_certificate_log_root`
The directory to store all logs created by `certbot` during operation, commonly set to `var/log/letsencrypt`.

#### `app_certificate_provisioning_username`
The directory to store all logs created by `certbot` during operation, commonly set to `var/log/letsencrypt`.