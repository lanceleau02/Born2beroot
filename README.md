<div align="center">

<h1>Born2beroot</h1>

<a href="https://imgflip.com/i/805z33"><img src="https://i.imgflip.com/805z33.jpg" width="400px" title="meme"/></a>

</div>

<p>Description:</p>

> This document is a System Administration related exercise.

<h2>✔️ Project's requirements</h2>

- A `SSH` service will be running on port `4242` only. For security reasons, it must not be
possible to connect using `SSH` as `root`.
- You have to configure your operating system with the `UFW` (or firewalld for Rocky)
firewall and thus leave only port `4242` open.
- The hostname of your virtual machine must be your login ending with 42 (e.g.,
wil42). You will have to modify this hostname during your evaluation.
- You have to implement a strong password policy.
- You have to install and configure `sudo` following strict rules.
- In addition to the `root` user, a user with your login as username has to be present.
- This user has to belong to the `user42` and `sudo` groups.

To set up a strong password policy, you have to comply with the following requirements:

- Your password has to expire every 30 days.
- The minimum number of days allowed before the modification of a password will
be set to 2.
- The user has to receive a warning message 7 days before their password expires.
- Your password must be at least 10 characters long. It must contain an uppercase
letter, a lowercase letter, and a number. Also, it must not contain more than 3
consecutive identical characters.
- The password must not include the name of the user.
- The following rule does not apply to the root password: The password must have
at least 7 characters that are not part of the former password.
- Of course, your root password has to comply with this policy.

To set up a strong configuration for your `sudo` group, you have to comply with the
following requirements:

- Authentication using `sudo` has to be limited to 3 attempts in the event of an incorrect password.
- A custom message of your choice has to be displayed if an error due to a wrong
password occurs when using sudo.
- Each action using sudo has to be archived, both inputs and outputs. The log file
has to be saved in the `/var/log/sudo/` folder.
- The `TTY` mode has to be enabled for security reasons.
- For security reasons too, the paths that can be used by sudo must be restricted. Example: `/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin`

Finally, you have to create a simple script called `monitoring.sh`. It must be developed in `bash`. At server startup, the script will display some information (listed below) on all terminals every 10 minutes (take a look at wall). The banner is optional. No error must be visible. Your script must always be able to display the following information:

- The architecture of your operating system and its kernel version.
- The number of physical processors.
- The number of virtual processors.
- The current available RAM on your server and its utilization rate as a percentage.
- The current available memory on your server and its utilization rate as a percentage.
- The current utilization rate of your processors as a percentage.
- The date and time of the last reboot.
- Whether `LVM` is active or not.
- The number of active connections.
- The number of users using the server.
- The IPv4 address of your server and its MAC (Media Access Control) address.
- The number of commands executed with the `sudo` program.

<h2>🧰 Toolbox</h2>

- [Born2BeRootTester](https://github.com/Pixailz/Born2BeRootTester)

<h2>📚 Resources</h2>

- [Tutorial of Baigalmaa Baatar on Medium (in english)](https://baigal.medium.com/born2beroot-e6e26dfb50ac)
