This challenge is command injection challenge with too many filters :).

Challenge description---

![Alt Text](https://i.imgur.com/uf0JkE4.png)

Challenge url--

![Alt Text](https://i.imgur.com/wQRRDvD.png)

Looking at the source code, you can see our payload is in sed command. Since these characters (";", "|", "&" ) are banned, we can execute two command. So we have to inject our command in sed. We can't also use these characters ("$" and "`"). After googling awhile, I found that we can also run command as `<addr>`((command)). 



