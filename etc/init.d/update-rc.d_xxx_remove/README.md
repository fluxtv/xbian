After ```apt-get install upstart plymouth mountall``` we have few scripts as duplicities. 
Those needs to be uninstalled with "update-rc.d [name] remove".
because of dependencies, /etc/init.d files needs to be updated. updated files are in up dir.


```
for f in $(ls); do 
    
        if [ $f != "README.md" ]; then
		update-rc.d $f disable
		update-rc.d -f $f remove
	fi

done
```
