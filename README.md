# NSH / VxLAN Tool

This is a modified version of https://github.com/opendaylight/sfc/blob/master/sfc-test/nsh-tools/vxlan_tool.py written by Yi Yang and Reinaldo Penno

This code was modified to

    run with Python 2.7
    swap the IP SA and DA when forwarding.
    Work for either UDP port 4790 or 6633
    Don't forward NSH frames unless service index is > 1
    Added verbose option to turn off prints when in forward mode

Options:

    -i: Interface to receive, and optionally send packets on
    -d: Mode: 'dump' or 'forward'. Default is dump.
    -v: Verbose: 'on' or 'off'. Default is 'on', and 'off' only works in 'forward' mode.

Example Use:

sudo python vxlan_tool.py -i 'eth1' -d 'forward' -v 'on'


