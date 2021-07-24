
# Record Keeping

## Note taking

There are five different main types of information that need to be noted down:

1. Newly discovered information
2. Ideas for further tests and processing
3. Scan results
4. Logging
5. Screenshots

### 1. Discovered Information

This represents general information, such as new IP addresses, usernames, passwords, source code, etc., that is identified and are related to the penetration testing engagement and process.

This is often obtained through OSINT, active scans, and manual analysis of the given information resources and services.

### 2. Processing

A lot of different information will be discovered during penetration testing that may require adapting the approach. These results may give ideas for subsequent steps to be taken, and other vulnerabilities or misconfigurations may be forgotten or overlooked.

It is a good habit to note down any thing seen that should be investigated as part of any penetration test.
[Obsidian](https://obsidian.md) is a useful notetaking tool that links various markdown files and acts as a knowledge base.

### 3. Results

Results collected after scans and other steps can often be considerable. It is easy to feel overwhelmed given the amount of information presented. While not all information is critical, it is important that all of it be recorded and kept, should some prove useful later on, as well as for general record keeping and documentation.

### 4. Logging

Logging is essential for documentation and traceability. For this, *script* and *date.Date* can be used to display the exact date and time of each command in the command line. With the help of *script*, every command and result is saved in a background file. To display the date and time, replace the PS! variable in .bashrc with the following command.

    PS1="\[\033[1;32m\]\342\224\200\$([[ \$(/opt/vpnbash.sh) == *\"10.\"* ]] && echo \"[\[\033[1;34m\]\$(/opt/vpnserver.sh)\[\033[1;32m\]]\342\224\200[\[\033[1;37m\]\$(/opt/vpnbash.sh)\[\033[1;32m\]]\342\224\200\")[\[\033[1;37m\]\u\[\033[01;32m\]@\[\033[01;34m\]\h\[\033[1;32m\]]\342\224\200[\[\033[1;37m\]\w\[\033[1;32m\]]\n\[\033[1;32m\]\342\224\224\342\224\200\342\224\200\342\225\274 [\[\e[01;33m\]$(date +%D-%r)\[\e[01;32m\]]\\$ \[\e[0m\]"

To start logging with script (Linux) or [Start-Transcript](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.host/start-transcript?view=powershell-7.1) (Windows), use the following command and rename it according to needs. It is recommended to define a certain format in advance after saving individual logs.

> Script

    user@computer[/home]$ script 03-21-2021-0200pm-exploitation.log

> Start-Transcript

    C:\> Start-Transcript -Path "C:\Pentesting\03-21-2021-0200pm-exploitation.log"

    Transcript started, output file is C:\Pentesting\03-21-2021-0200pm-exploitation.log

    C:\> Stop-Transcript

This will automatically sort logs and remove the need for manual examination. This also allows later examination and analysis, identifying what commands may be turned into scripts for better efficiency.

It should also be notted that terminal emulators such as TMux and Terminator allow automated logging and output of commands. Any tools that do not allow normal logging should be redirected.

### 5. Screnshots

These serve as record and proof of results, necessary of prrof of concent and documentation. Tools for this include [Flameshot](https://github.com/flameshot-org/flameshot) and [Peek](https://github.com/phw/peek).
