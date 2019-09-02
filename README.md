# Gluipertje 2b2t Queue Proxy
A proxy node.js server to connect into the 2b2t queue to get further ahead into the queue without having your mc client turned on

# How to install
1. Download [node.js](https://nodejs.org/en/download/) and install it. On non-windows platforms, you also need npm.
2. Download this repository as a zip, then, unzip it.
3. Copy secrets.json-example and name it secrets.json. Fill out your minecraft information in the file. Note that you must use your email adress and not your minecraft username.
4. If you so wish, edit the configuration in config.json. (On Linux ports below 1024, including port 80, require you to run the program with administrator rights.)
5. For trust reasons, *this tool does not update automatically*. Check back here once in a while to see if there are any updates.


# How to use
1. read the code to ensure we're not stealing your credentials. we're not, but you shouldn't take our word for it. If you don't know how to read it, downloading stuff off the internet and giving it your password is probably a bad idea anyway.
4. run `npm start`
5. a browser window should open. You can close it if you want at any moment, and you can access it again at adress http://localhost
6. press the "Start queing" button. The queue position indicator auto-updates, but sometimes it takes a while to start counting (like 1 min).
7. once the queue reaches a low number, connect to the minecraft server at address `localhost`. Currently, you have to connect BEFORE reaching the end of the queue or you will not spawn in the world correctly (I'm told that sneaking around and right-clicking things eventually makes you spawn correctly but I was not able to verify that).
8. after you log off, click the "stop queuing" button. This is really important, as you will not actually disconnect from 2b2t until you do that.
9. MAKE SURE you connect before the queue end or the minecraft server proxy will stop (known bug)

# How to use (On a server)
1. using port 80 for the webserver usually results in problems so we advise changing it to something like '8080'
2. make sure you opened the webserver port and minecraft port (tcp:25565, tcp:80)
3. in 'config.json' set 'openBrowserOnStart' to false
4. now run `npm start` and connect to your external server IP and after that your selected port via a webbrowser
`example: 108.16.17.7/80`
5. now just continue with the default start tutorial

# Known bugs
1. You get kicked much sooner for being afk if you use this tool
2. Riding entities is not working
3. If you fish, your fishing line is not shown
4. These are bugs caused by connecting via proxy, these cant be fixed.

# Credits
Thanks to 'The moon is a cheese' for the original node.js server proxy, https://github.com/themoonisacheese/2bored2wait
