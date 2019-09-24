# Step 1: Create a Samba user matching your Linux credentials

`smbpasswd -a MyUsername`

# Step 2: Use [`chown` and `chmod`](https://www.cyberciti.biz/faq/how-to-use-chmod-and-chown-command/) to ensure your Linux account has access to the shared folder

`sudo chown MyUsername /SharedFolderPath`

and [then](https://www.computerhope.com/unix/uchmod.htm):

`sudo chmod 770 /SharedFolderPath`

# Step 3: Edit `smb.conf` as below:

    [global]
       security = user

       #In addition to the rest of what's there for [global]

    [SharedFolderName]
      comment = Insert comment here
      read only = no
      browseable = yes
      writable = yes
      valid users = MyUsername
      path = /SharedFolderPath
      create mask = 0770
      directory mask = 0770
      force user = MyUsername

Source: https://www.reddit.com/r/debian/comments/csc3vt/buster_i_can_access_smb_share_from_windows_10/exe050g/