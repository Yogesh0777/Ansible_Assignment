# Ansible_Assignment
Q.  Directory stracture of roles?
Ans. The concept of an Ansible role is simple; it is a group of variables, tasks, files, and handlers stored in a standardised file structure. Above all, 
      we always have the freedom to write our tasks and variable.
    Defaults:
    The defaults directory is for defining the variable defaults. The variables in default have the lowest priority thus becoming easy to override. If definition     of a variable is nowhere else, the variable in defaults/main.yml will be used.

    Files:
    We use the files directory to add files that are needed by provisioning machine, without modification. Mostly, we use copy task for referencing files in the       files directory. The most interesting part about this is that Ansible does not require a path for resources stored in files directory when working in the         role.

    Handlers:
    The handlers directory is used for storing Ansible handlers. Handlers are tasks that may be flagged during a play to run at the play’s completion. We can have      as many and as few handlers as we need.
 
    Meta:
    We use the meta directory to store authorship information which is useful if we choose to publish our role on galaxy.ansible.com. The metadata of an Ansible       role consists of author, supported platforms, and dependencies.

    Tasks:
    The task directory is where we write most of our roles which includes all the tasks our role will perform. We write each series of tasks in a separate file       and include them into the main.yml file in the tasks directory.

   Templates:
   We use the template directory to also add files to our machine(similar to files directory). Only difference between template and files directories is that the    template directory supports alteration (modification). Jinja2 language to used to create these alteration. Most software configuration files become templates.

   Tests:
  We can use the tests directory if we have built and automated testing process around our role. This directory contains a sample inventory and a test.yml file.

  Vars:
  This is where we create variable files that define necessary variables for our role. The variables defined in this directory are meant for role internal use        only. Also, it is a good idea to namespace our role variable names, to prevent potential naming conflicts with variables outside of our role.

Q. What is scp work in ssh?
Ans. The Secure Copy Protocol, or SCP, is a file transfer network protocol used to move files onto servers, and it fully supports encryption and authentication.        SCP uses Secure Shell (SSH) mechanisms for data transfer and authentication to ensure the confidentiality of the data in transit.

Q. roles create command?
Ans sudo ansible-galaxy init rolename.

Q. what is inventories?
Ans. The Ansible inventory file defines the hosts and groups of hosts upon which commands, modules, and tasks in a playbook operate. The file can be in one of           many formats depending on your Ansible environment and plugins. The inventory file can list individual hosts or user-defined groups of hosts.

Q. what is playbook and its command?
Ans. Playbooks are the files where Ansible code is written. Playbooks are written in YAML format. YAML stands for Yet Another Markup Language. Playbooks are one        of the core features of Ansible and tell Ansible what to execute.Playbooks contain the steps which the user wants to execute on a particular machine.

    command...ansible-playbook playbookname.yml

Q. What is yaml?
Ans. YAML stands for Yet Another Markup Language. Playbooks are one of the core features of Ansible and tell Ansible what to execute. They are like a to-do list        for Ansible that contains a list of tasks. Playbooks contain the steps which the user wants to execute on a particular machine.

Q. what is module?
Ans. A module is a reusable, standalone script that Ansible runs on your behalf, either locally or remotely. Modules interact with your local machine, an API, or      a remote system to perform specific tasks like changing a database password or spinning up a cloud instance.

Q.   what is Tasks?
Ans.   A task is the smallest unit of action you can automate using an Ansible playbook. Playbooks typically contain a series of tasks that serve a goal, such as       to set up a web server, or to deploy an application to remote environments. Ansible executes tasks in the same order they are defined inside a playbook.


Q. What is hosts?
Ans. In ansible, host files are those files that are used for storing information about remote nodes information, which we need to manage. This file can be placed       but its location needs to be set up either in a configuration file or give on the command line.











