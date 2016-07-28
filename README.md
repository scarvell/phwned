# Phwned
### Grandstream Backdoor Removal Tool

Grandstream GXV3275 Android VoIP phones come with a vendor backdoor by default when unpacked out of the box. This tool attempts to automate the removal of this backdoor by exploiting remote code execution vulnerabilities that we discovered in the phone. The security fixes for these remote code execution vulnerabilities do not remove the backdoor and therefor must only be applied after running this tool.

For more information, go to [http://phwned.com](http://phwned.com).

**NOTE:** This has only been successfully tested with the **kernel version <= 1.0.1.9**. Later versions (I've tested up to **v1.0.1.12**) seem to put the file system into read-only. You will have to try roll back for this to work if you're running a later kernel.

## Requirements
- Python
- Paramiko
- GXV3275 Phone running Kernel 1.0.1.9

## Arguments

    --host=<host> Phone IP Address/Hostname
    --port=<port> (optional) Port of the running SSH service. Default: 22
    --pass=<password> (optional) SSH password for phone. Default: admin
    --user=<username> (optional) SSH username for phone. Default: admin

## Usage

    $ ./phwned --host=10.0.0.13

         __                                     __
        /\ \                                   /\ \
     _____\ \ \___   __  __  __    ___      __   \_\ \
    /\ '__`\ \  _ `\/\ \/\ \/\ \ /' _ `\  /'__`\ /'_` \
    \ \ \L\ \ \ \ \ \ \ \_/ \_/ \/\ \/\ \/\  __//\ \L\ \
     \ \ ,__/\ \_\ \_\ \___x___/'\ \_\ \_\ \____\ \___,_\
      \ \ \/  \/_/\/_/\/__//__/   \/_/\/_/\/____/\/__,_ /
       \ \_\
        \/_/
    =============================================================
    Grandstream GXV3275 Backdoor Remover - http://phwned.com
    Created by: Brendan Scarvell <bscarvell@gmail.com>
    =============================================================

    [+] Starting phwnage
    [+] Attempting shell breakout..
    [+] w00t root
    [+] Checking for backdoor..
    [!] Backdoor detected!
    [+] Removing backdoor..
    [+] Backdoor removed successfully
    [+] Finished
