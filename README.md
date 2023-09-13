# My Ansible Playbook

## Available Tags

- `groups`:
    - Adds the user to the specified groups: [task](tasks/add_use_to_group.yml)
- `sudoers`:
    - Removes the password requirement from the sudoers file: [task](tasks/no_pass_sudoers.yml)
- `timezone`:
    - Sets the timezone: [task](tasks/set_timezone.yml)
- `pacman`:
    - Update pacman config: [task](tasks/configure_pacman.yml)
    - Install packages: [task](tasks/install_pacman_packages.yml)
        - Packages: [var](vars/pkgs.yml)
- `git`:
    - Install git: [task](tasks/install_git.yml)
- `paru`:
    - Install paru: [task](tasks/install_paru.yml)
    - Install AUR packages: [task](tasks/install_aur_packages.yml)
        - Packages: [var](vars/pkgs.yml)
- `gpg`:
    - Configure GPG Agent: [task](tasks/configure_gpg.yml)
    - Download GPG Key using YubiKey: [task](tasks/configure_gpg.yml)
- `services`:
    - Enable System Services: [task](tasks/enable_system_services.yml)
        - sshd
        - docker
        - cronie
        - pcscd
    - Enable User Services: [task](tasks/enable_user_services.yml)
        - syncthing
- `cron`:
    - Configure Crontab: [task](tasks/configure_crontab.yml)
        - Borg
        - Arch Linux Keyring
        - fstrim
- `shell`:
    - Sets `zsh` as default shell: [task](tasks/set_zsh_as_default_shell.yml)

- `all`:
    - All of the above

## Usage

```bash
ansible-galaxy install -r requirements.yaml
ansible-playbook install.yaml --tags="all" # or specify tags
```
