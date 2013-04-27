after 

apt-get install upstart plymouth mountall

we have few scripts as duplicities. those needs to be uninstalled with

"update-rc.d [name] remove"

because of dependencies, /etc/init.d files needs to be updated. updated files are in up dir.
