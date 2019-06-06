# GLUIP-2B2T-Queue-Proxy
A proxy node.js server to connect into the 2b2t queue to get further ahead into the queue without having your mc client turned on

# How to install
1. Download [node.js](https://nodejs.org/en/download/) and install it. On non-windows platforms, you also need npm.
2. Download this repository as a zip, then, unzip it.
3. Open a terminal and navigate to the folder you downloaded it
4. Run `npm install`
5. Copy secrets.json.example and name it secrets.json. Fill out your minecraft information in the file. Note that you must use your email adress and not your minecraft username.
6. If you so wish, edit the configuration in config.json. (On Linux ports below 1024, including port 80, require you to run the program with administrator rights.)
7. For trust reasons, *this tool does not update automatically*. Check back here once in a while to see if there are any updates.


# How to use
1. read the code to ensure i'm not stealing your credentials. i'm not, but you shouldn't take my word for it. If you don't know how to read it, downloading stuff off the internet and giving it your password is probably a bad idea anyway.
4. run `npm start`
5. a browser window should open. You can close it if you want at any moment, and you can access it again at adress http://localhost
6. press the "Start queing" button. The queue position indicator auto-updates, but sometimes it takes a while to start counting (like 1 min).
7. once the queue reaches a low number, connect to the minecraft server at address `localhost`. Currently, you have to connect BEFORE reaching the end of the queue or you will not spawn in the world correctly (I'm told that sneaking around and right-clicking things eventually makes you spawn correctly but I was not able to verify that).
8. after you log off, click the "stop queuing" button. This is really important, as you will not actually disconnect from 2b2t until you do that.
