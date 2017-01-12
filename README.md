# fixcPanelhomepermissions
Fixes home directory user permissions for centOS/cPanel systems

## Credit to Source

This was originally found at [The cPanel Admin](http://thecpaneladmin.com/fix-account-permissions/)

I added this version on GitHub

## Usage

Download the shell script to your server, then make to sure to make it executable:

```
chomd 755 fixperms.sh
chomd +X fixperms.sh
```

You can pass in a user list manually like this:

```
./fixperms.sh user1 user2 user3
```

You can also run a server-wide loop like this:

```
for i in `ls -A /var/cpanel/users` ; do ./fixperms.sh $i ; done
```