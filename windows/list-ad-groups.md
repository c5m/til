# List AD Groups
It is possible to see the AD groups you are a member of using
~~~
net user <userName> /domain
~~~
or even better
~~~
whoami /groups
~~~
and you can save the output to a file using
~~~
whoami /groups > ad-groups.txt
~~~

To see the members of a given group use
~~~
net group /domain <group-name>
~~~
or alternatively run `Rundll32 dsquery.dll OpenQueryWindow` if
you want a GUI.