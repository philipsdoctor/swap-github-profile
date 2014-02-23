swap-github-profile
===================

short script to swap profiles

Prerequisites
===================

Uses [lein-exec] (https://github.com/kumarshantanu/lein-exec) for scripting.

Assumes are using multiple ssh hosts in ~/.ssh/config like this

    Host github-WORK
      HostName github.com
      User git
      IdentityFile ~/.ssh/id_rsa_WORK

Uses
==================

Modify the maps as needed:

    (def work {:username "some-work-username"
               :email "some-work-email"
               :origin-host "github-WORK"})

Then call the script from inside the git repo you wish to swap:

    [~/myproject] $ swap-github-profile work


