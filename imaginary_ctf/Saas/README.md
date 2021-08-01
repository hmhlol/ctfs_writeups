This challenge is command injection challenge with too many filters :).

Challenge description---

![Alt Text](https://i.imgur.com/uf0JkE4.png)

Challenge url--

![Alt Text](https://i.imgur.com/wQRRDvD.png)

Looking at the source code, you can see our payload is in sed command. Since these characters `; | &` are banned, we can't execute two command. So we have to perform our injection in sed command. We can't also use these characters ("$" and backtick ). After googling awhile, I found that we can also run command as `((command))`. We can use `/e` modifier to excute our command. So the paylaod begin `"s/Lorem/((whoami))/e"`. But our command didn't execute.

![Alt_Text](https://i.imgur.com/cScOaqu.png)

After testing in local, I found that we need to replace all characters in the file with our command. So our payload become `"s/.*/((whoami))/e"`.

![Alt_Text](https://i.imgur.com/rv8fYr9.png)

Boom! Our command is now executed. Let's read the flag file. We can bypass `cat & flag` in blacklist with single quote  like `c'a't & f'l'ag`. Our final payload become `"s/.*/((c'a't f'l'ag.txt))/e"`.

![Alt_Text](https://i.imgur.com/UGtTuPo.png)

Flag: `ictf{:roocu:roocu:roocu:roocu:roocu:roocursion:rsion:rsion:rsion:rsion:rsion:_473fc2d1}`


Thank you for reading. Hope you enjoy this. :cowboy_hat_face: :cowboy_hat_face:



