Following this tutorial: https://docs.ansible.com/ansible/2.6/scenario_guides/guide_aws.html

Stuff not in the tutorial
* Put secrets in vars file: https://docs.ansible.com/ansible/latest/user_guide/playbooks_variables.html
* "group: test" created in AWS UI, given SSH-from-anywhere access
* manual key created in AWS UI, download pem, change permissions, add to gloabl ansible cfg as default
* Need to go look up correct ami id for your region
* gather facts == setup step; change to false, wait for connection first, then setup
* The NTP service is named chronyd instead of ntpd on this image; it's just a hello world status check so it doesn't matter that much

Possible improvements
* Configure manual key pem for this playbook, rather than ansible global default cfg
* Actually do something with the machines instead of just starting them
* Add a playbook to terminate instances, I was just doing that through the UI each time. Maybe setting exact count to 0 is enough?
