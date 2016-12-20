Serial Console
=========

Setup of the Serial Console.

Requirements
------------

None

Role Variables
--------------

### serial sonsole
* `serial_console_serial_unit`: 0
* `serial_console_serial_port`: ttyS0
* `serial_console_serial_speed`: 115200

### grub
* `serial_console_grub_terminal`: "console serial"

### inittab
* `serial_console_inittab_runlevels`: 23

### upstart
* `serial_console_upstart_start`: 345
* `serial_console_upstart_stop`: S016

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: hudecof.serial-console }

Adding more OS and versions
---------------------------
At this time I do not have more OS/version matrix to test.


Add file for your distribution and release into **vars** direcrory. For thr naming convetions see **tasks/main.yml**. Add tasks to be execute in the `serial_console_tasks` variable. Add any other needed variables, seeother files for reference.


License
-------

BSD

Author Information
------------------

Peter Hudec