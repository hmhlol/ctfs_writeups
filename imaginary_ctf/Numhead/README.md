This is `api` challenge with no vulnerablity. May be `the purpose of this challenge is to understand the code`.

Challenge description--

![Alt_Text](https://i.imgur.com/guIOWhJ.png)

Challenge url--

![Alt_Text](https://i.imgur.com/JzI2H7s.png)

`--Solution--`

`1# Create user using post request to "/api/user/new-token" by adding header "Authorization: 0nlyL33tHax0rsAll0w3d"('0nlyL33tHax0rsAll0w3d' is in config.py')`

![Alt_Text](https://i.imgur.com/jmPount.png)

`2# Post request to "/api/user/nothing-here" with "Authorization: (Your user token)". Your will See '{"detail": "requests were the same :rooFrozen:"}'`

![Alt_Text](https://i.imgur.com/qxVo8Jd.png)

`3# Add one random header(such as 'X-Forward-For: 127.0.0.1') and request again "/api/user/nothing-here"`

![Alt_Text](https://i.imgur.com/pgWxWR0.png)

`4# If you see '{"detail": "i'm being hacked :rooNobooli: :banhammer:"}', that mean you get 100 points. You can check by going to "/api/user/points"`

![Alt_Text](https://i.imgur.com/igzutXn.png)

`5# Repeat doing this(#3) until you get 1000 points.`

![Alt_Text](https://i.imgur.com/D5hsjoK.png)

`6# When you get 1000 points, go to "/api/admin/flag" and enjoy your flag. :)`

![Alt_Text](https://i.imgur.com/R3SBn5p.png)

Flag: `ictf{b3aT_tH3_g@Me_???}`

Thank you for reading. :cowboy_hat_face: :cowboy_hat_face:
