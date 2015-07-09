This repository contains some AppArmor profiles for Atlassian software.
Absolutely no support is provided for the profiles or the instructions found in this readme file.

----
## Usage
If you are not using the default installation paths for a product then you will need to
modify the profiles before use.

Additionally, these profiles are currently intended to be used in combination with `aa-exec`.
See the `aa-exec` man page for details on how to use it.


## Installing
To install these profiles run the following

    sudo cp -a abstractions/atlassian /etc/apparmor.d/abstractions/
    sudo cp confluence /etc/apparmor.d/
    sudo cp crowd /etc/apparmor.d/
    sudo cp jira /etc/apparmor.d/
    sudo chown root. /etc/apparmor.d/confluence /etc/apparmor.d/crowd /etc/apparmor.d/jira
    sudo aa-complain /etc/apparmor.d/confluence
    sudo aa-complain /etc/apparmor.d/crowd
    sudo aa-complain /etc/apparmor.d/jira


## Contributing
Fork this repository and raise a pull request.
