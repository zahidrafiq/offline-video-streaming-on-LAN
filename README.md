# offline-video-streaming-on-LAN
This Repositry is for offline Video streaming on Local Area Network.
Required Tools
1. Nodejs
2. Fiddler (To Access from other stsyem on LAN)

Setup to Follow:
1. Clone/Download this repositry.
2. In main Folder(That contains index.js file), run Command Prompt.
3. Run following command:
    node index.js
4. Open Browser and go to:
    localhost:8080 
    and (Allow Camera and microphone access)
    Local Stream should be visible to you.
5. In order to access form other system we have to install fiddler in one of the systems i.e Pc1.
    (To Download Fiddler: https://www.telerik.com/fiddler)
    
    Demo video of Following Two Steps is available at: https://www.youtube.com/watch?v=ewYkIuRbyvU&t=
6. Open Fiddler => Rules(in toolbar) => Select "Customize Rule" option(File will be opened).
    In "OnBeforeRequest(oSession: Session)" method, Add Following Two lines:
  if(oSession.host == "IP:Port")
      oSession.host = "localhost:8080";
      (IP: IP of Your Machine on which Fiddler is installed, Port: Any Available Port)
 7. In Pc2 Browser, Type http://IP:Port (IP & Port Specified in Fiddler Rules File of Pc1)
 
 Note: During the Process of Streaming Fiddler must be running on Pc1(in which node as well running).
 
 
 
      

   


