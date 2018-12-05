# Find Jar
To find the jar that a certain class resides in use
```sh
for f in `find . -name '*.jar'`;  do echo $f && jar tvf $f | grep -i $1; done
```

Or use https://www.findjar.com

Alternative software is
http://tattletale.jboss.org/