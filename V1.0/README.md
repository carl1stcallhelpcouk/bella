#===== sshup ==================================================================#
#                                                                              #
# FILE:         sshupV1.sh                                                     #
#                                                                              #
# USAGE:        sshupV1.sh [-o | --host <host>] [-d | --debug] [-h | --help]   #
#               [-q | --quiet] [-v | --verbose] [-w | --wait] [-c | --connect] #
#               [-u | --wakeup] [-t | --timeout <timeout>]"                    #
#                                                                              #
#               (see sshup.usage for details)                                  #
#                                                                              #
# DESCRIPTION:  Check host availability, and optionally connect via ssh to     #
#               specified host.  All options can be set from the command line  #
#               (see sshup.usage for details.), from ~/.sshup.conf. or from    #
#               /etc/sshup.conf.                                               #
#                                                                              #
#               Command line options overide ~/.sshup.conf, which in turn      #
#               overides /etc/sshup.conf.                                      #
#                                                                              #
# OPTIONS:      See the ’sshup.usage’ file for details.                        #
#                                                                              #
# REQUIREMENTS: openssh-client, ping, gawk                                     #
#                                                                              #
# BUGS:         Report all bugs and/or sugestions to bugs@1stcallhelp.co.uk    #
#                                                                              #
# AUTHOR:       <Carl McAlwane>carl@1stcallhelp.co.uk                          #
#                                                                              #
# COMPANY:      1stcallhelp.co.uk                                              #
#                                                                              #
# VERSION:      1.0                                                            #
#                                                                              #
# CREATED:      11.05.2016                                                     #
#                                                                              #
# REVISION:     1.0.0.2016                                                     #
#                                                                              #
# COPYRIGHT:    (C)2000-2016 1st Call Group.  All rights reserved.             #
#                                                                              #
# TODO:         1. Comment code.                                               #
#               2. Standardised variable names and comments.                   #
#               3. Move standard functions and constants to sshup.shinc.       #
#               4. Format email in html.  Maybe use ansi2html.sh ??            #
#               5. Perhaps add an option to format email as plain text.        #
#               6. Incorparate wakeup scripts.                                 #
#               7. Standardise how ouput is sent to fnOutput.  (probably using #
#                   printf 2>&1 | fnOutput but maybe echo -e 2>&1 | fnOutput)  #
#                                                                              #
#               8. Standardise comments.                                       #
#               9. Impliment a ${optLogFile} for logging.                      # 
#                                                                              #
#==============================================================================#
