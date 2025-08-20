# Ansible Connection Test

This project is designed to test connectivity to Linux machines using Ansible. It includes a playbook that utilizes the `ping` module to verify connections to specified hosts.

## Project Structure

- `playbook.yml`: The Ansible playbook that defines tasks for testing connectivity.
- `inventory`: A file listing the target Linux hosts for the playbook.
- `group_vars/all.yml`: Variables that apply to all hosts in the inventory, including connection parameters.
- `README.md`: Documentation for the project.

## Prerequisites

- Ansible installed on your control machine.
- SSH access to the target Linux machines.
- Properly configured inventory file with the correct hostnames or IP addresses.

## Running the Playbook

1. Ensure that your inventory file is correctly set up with the target hosts.
2. Navigate to the project directory:
   ```
   cd ansible-connection-test
   ```
3. Run the playbook using the following command:
   ```
   ansible-playbook -i inventory playbook.yml
   ```

## Notes

- Make sure to adjust the `group_vars/all.yml` file to include any necessary connection parameters.
- The playbook will use the `ping` module to test connectivity. If the connection is successful, you will see a success message for each host.