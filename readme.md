This is a list of IP's and subnets that I've observed doing one thing or another that offended me. Therefore, I don't want them talking to my hosts any longer. Use this list as you will, but please give credit when you do as I've spent a lot of time trawling my logs from around the interwebs to create it. Currently the list is very simple. It's a list of CIDRs that I parse during host build and on other occasions to update my firewalls.

TODO: Make it a CSV or something similar that can be parsed automatically during host build and read by humans to include both a reason and a nethost and/or ASN for each of the blocks. - STATUS: Partial complete.

I'm using the following line to update ufw on certain hosts:
for i in `sed '1d' $path$file |cut -d',' -f 1`; do echo "Updating range ${i}"; ufw reject from ${i} to any; done

Obviously this is in a script, but you can change it how you like.

I can be reached on the twitter and here via my handle, DFWInfoStudent.
