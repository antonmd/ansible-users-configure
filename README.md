## Usage:

Create a file named like your host group in the inventory file. In the file, create a list of users with parameters as in the example:

    names:
      test:    
	    ssh_key: ./keys/test.pub
	    sudo: 'false'
	    action: 'create'

*test* - user`s name
*ssh_key: ./keys/test.pub* - path to ssh public key
*sudo* - make user sudoers or not, can be 'true' or 'false'
*action* - what to do with the user - create or delete, can be 'create' or 'delete'

If you create a sudo user it will have password entry disabled when executing sudo commands.
You can add multiple users, each with different parameters.