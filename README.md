## 2.1 Original code of broadcast chat
#### Server
![](https://media.discordapp.net/attachments/1054028087551078452/1237674682203897866/image.png?ex=663c81df&is=663b305f&hm=fe9066287a23735703d9751a2558c3cf86e6ca094c374dcc023957fe0dbf5894&=&format=webp&quality=lossless&width=1021&height=322)
#### Client
![](https://media.discordapp.net/attachments/1054028087551078452/1237674741700104253/image.png?ex=663c81ed&is=663b306d&hm=7ab421bf7d67e2178096c6ab3714093eaa173412f4ad967ddd373b520f63ca03&=&format=webp&quality=lossless&width=973&height=242)
![](https://media.discordapp.net/attachments/1054028087551078452/1237674765901234240/image.png?ex=663c81f3&is=663b3073&hm=39206b4b596b2227cb0c0d53b6965335559ca2c6ac4f7d06e5a648122ca43ce9&=&format=webp&quality=lossless&width=988&height=278)
![](https://media.discordapp.net/attachments/1054028087551078452/1237674795806752818/image.png?ex=663c81fa&is=663b307a&hm=8e05c102731bcfe250713dce51a0f1452a1c38826ad5bc198c2cb3192c5dee79&=&format=webp&quality=lossless&width=972&height=285)
<br>
To run, just run `cargo run --bin <file_name>`. When I type some text in a client, the text will also be sent to other clients and server.

## 2.2 Modifying the websocket port
![](https://media.discordapp.net/attachments/1054028087551078452/1237680441436274698/image.png?ex=663c873c&is=663b35bc&hm=fea3c1f7b1d6480b6d9833206d0d814ee1df8fd9005134c1a2fc814814723994&=&format=webp&quality=lossless&width=1176&height=226)
Other than the client.rs file, I also changed the port in server.rs file, specifically in line 43 and 45. The protocol in server.rs file is different from the client.rs where client.rs uses a websocket, while server.rs uses a TCP protocol.

## 2.3 Small changes. Add some information to client
![](https://media.discordapp.net/attachments/1054028087551078452/1237682715415941163/image.png?ex=663c895a&is=663b37da&hm=3cb66f11345dce0e6a294c2c168c84acc5548a9dd453953552b2a3e6629f8e02&=&format=webp&quality=lossless&width=1197&height=343)
![](https://media.discordapp.net/attachments/1054028087551078452/1237682737314271303/image.png?ex=663c895f&is=663b37df&hm=7b7a0dc35dfe7ac09e2d7569eb58fb598a5bc0c8d096d002ca010f200d8576a2&=&format=webp&quality=lossless&width=687&height=172)
![](https://media.discordapp.net/attachments/1054028087551078452/1237682773121175583/image.png?ex=663c8968&is=663b37e8&hm=0ea00ea7d8556b81364d744ac50c1917fdd81b5689981ba701e9ec9d47abc49b&=&format=webp&quality=lossless&width=687&height=192)
![](https://media.discordapp.net/attachments/1054028087551078452/1237682811935391764/image.png?ex=663c8971&is=663b37f1&hm=6a54bcc87f5147c3d958c02091537b29cc136ae4543e3dd72c8c94e2af55960e&=&format=webp&quality=lossless&width=687&height=191)
I added some information to the client where they will send message not only the text, but with their address as well. On the other hand, I added `Ian's Computer` to the server to give more information.