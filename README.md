# cloud_engr-Ass1
Your login name: altschool i.e., home directory /home/altschool. The home directory contains the following sub-directories: code, tests, personal, misc Unless otherwise specified, you are running commands from the home directory.

osboxes@osboxes:~$ sudo useradd -m -s /usr/bin/bash altschool
osboxes@osboxes:~$ ls
Desktop  Documents  Downloads  Music  Pictures  Public  snap  Templates  Videos  vim-editor
osboxes@osboxes:~$ sudo passwd altschool
New password: 
Retype new password: 
passwd: password updated successfully
osboxes@osboxes:~$ sudo usermod -aG sudo altschool
osboxes@osboxes:~$ sudo su -altschool
su: invalid option -- 'a'
Try 'su --help' for more information.
osboxes@osboxes:~$ sudo su - altschool
To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

altschool@osboxes:~$ mkdir code tests personal misc
altschool@osboxes:~$ cd /home/altschool/tests
altschool@osboxes:~/tests$ cd..
cd..: command not found
altschool@osboxes:~/tests$ cd ..
altschool@osboxes:~$ cd tests
altschool@osboxes:~/tests$ cd ..
altschool@osboxes:~$ echo Hello A > /home/altschool/misc/fileA
altschool@osboxes:~$ cat /home/altschool/misc/fileA
Hello A
altschool@osboxes:~$ pwd
/home/altschool
altschool@osboxes:~$ cd misc
altschool@osboxes:~/misc$ touch fileB
altschool@osboxes:~/misc$ cp fileA fileC
altschool@osboxes:~/misc$ mv fileB fileD
altschool@osboxes:~/misc$ ls
fileA  fileC  fileD
altschool@osboxes:~/misc$ tar -cvf misc.tar *
fileA
fileC
fileD
altschool@osboxes:~/misc$ gzip misc.tar
altschool@osboxes:~/misc$ sudo useradd -m -s /usr/bin/bash/leiman
[sudo] password for altschool: 
useradd: Warning: missing or non-executable shell '/usr/bin/bash/leiman'
Usage: useradd [options] LOGIN
       useradd -D
       useradd -D [options]

Options:
      --badnames                do not check for bad names
  -b, --base-dir BASE_DIR       base directory for the home directory of the
                                new account
      --btrfs-subvolume-home    use BTRFS subvolume for home directory
  -c, --comment COMMENT         GECOS field of the new account
  -d, --home-dir HOME_DIR       home directory of the new account
  -D, --defaults                print or change default useradd configuration
  -e, --expiredate EXPIRE_DATE  expiration date of the new account
  -f, --inactive INACTIVE       password inactivity period of the new account
  -g, --gid GROUP               name or ID of the primary group of the new
                                account
  -G, --groups GROUPS           list of supplementary groups of the new
                                account
  -h, --help                    display this help message and exit
  -k, --skel SKEL_DIR           use this alternative skeleton directory
  -K, --key KEY=VALUE           override /etc/login.defs defaults
  -l, --no-log-init             do not add the user to the lastlog and
                                faillog databases
  -m, --create-home             create the user's home directory
  -M, --no-create-home          do not create the user's home directory
  -N, --no-user-group           do not create a group with the same name as
                                the user
  -o, --non-unique              allow to create users with duplicate
                                (non-unique) UID
  -p, --password PASSWORD       encrypted password of the new account
  -r, --system                  create a system account
  -R, --root CHROOT_DIR         directory to chroot into
  -P, --prefix PREFIX_DIR       prefix directory where are located the /etc/* files
  -s, --shell SHELL             login shell of the new account
  -u, --uid UID                 user ID of the new account
  -U, --user-group              create a group with the same name as the user
  -Z, --selinux-user SEUSER     use a specific SEUSER for the SELinux user mapping
      --extrausers              Use the extra users database

altschool@osboxes:~/misc$ sudo passwd leiman
New password: 
BAD PASSWORD: The password contains the user name in some form
Retype new password: 
passwd: password updated successfully
altschool@osboxes:~/misc$ sudo passwd --expire 0 leiman
Usage: passwd [options] [LOGIN]

Options:
  -a, --all                     report password status on all accounts
  -d, --delete                  delete the password for the named account
  -e, --expire                  force expire the password for the named account
  -h, --help                    display this help message and exit
  -k, --keep-tokens             change password only if expired
  -i, --inactive INACTIVE       set password inactive after expiration
                                to INACTIVE
  -l, --lock                    lock the password of the named account
  -n, --mindays MIN_DAYS        set minimum number of days before password
                                change to MIN_DAYS
  -q, --quiet                   quiet mode
  -r, --repository REPOSITORY   change password in REPOSITORY repository
  -R, --root CHROOT_DIR         directory to chroot into
  -S, --status                  report password status on the named account
  -u, --unlock                  unlock the password of the named account
  -w, --warndays WARN_DAYS      set expiration warning days to WARN_DAYS
  -x, --maxdays MAX_DAYS        set maximum number of days before password
                                change to MAX_DAYS

altschool@osboxes:~/misc$ sudo useradd -s /usr/bin/sbash/nologin
useradd: Warning: missing or non-executable shell '/usr/bin/sbash/nologin'
Usage: useradd [options] LOGIN
       useradd -D
       useradd -D [options]

Options:
      --badnames                do not check for bad names
  -b, --base-dir BASE_DIR       base directory for the home directory of the
                                new account
      --btrfs-subvolume-home    use BTRFS subvolume for home directory
  -c, --comment COMMENT         GECOS field of the new account
  -d, --home-dir HOME_DIR       home directory of the new account
  -D, --defaults                print or change default useradd configuration
  -e, --expiredate EXPIRE_DATE  expiration date of the new account
  -f, --inactive INACTIVE       password inactivity period of the new account
  -g, --gid GROUP               name or ID of the primary group of the new
                                account
  -G, --groups GROUPS           list of supplementary groups of the new
                                account
  -h, --help                    display this help message and exit
  -k, --skel SKEL_DIR           use this alternative skeleton directory
  -K, --key KEY=VALUE           override /etc/login.defs defaults
  -l, --no-log-init             do not add the user to the lastlog and
                                faillog databases
  -m, --create-home             create the user's home directory
  -M, --no-create-home          do not create the user's home directory
  -N, --no-user-group           do not create a group with the same name as
                                the user
  -o, --non-unique              allow to create users with duplicate
                                (non-unique) UID
  -p, --password PASSWORD       encrypted password of the new account
  -r, --system                  create a system account
  -R, --root CHROOT_DIR         directory to chroot into
  -P, --prefix PREFIX_DIR       prefix directory where are located the /etc/* files
  -s, --shell SHELL             login shell of the new account
  -u, --uid UID                 user ID of the new account
  -U, --user-group              create a group with the same name as the user
  -Z, --selinux-user SEUSER     use a specific SEUSER for the SELinux user mapping
      --extrausers              Use the extra users database

altschool@osboxes:~/misc$ 
