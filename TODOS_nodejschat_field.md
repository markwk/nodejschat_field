# Todos:
These are just some thoughts, feel free to add and change

## Questions:
* What do you we need to do on Drupal end? 
* *Answer*: Implement Drupal 6 NodeJS API module 
* *Answer*: NodeJS API module should work well know for api with nodejs server.
* Working from 6.x-3.x branch of chatroom module?
* *Answer*: Doubtful, even 7.x-3.x still in dev, seems to be still too tightly integrated with Drupal
* 
* Good existing Node.JS + Socket.io chat server code?
* *Example*: https://github.com/endtwist/AjaxIM/
* *Example*: https://github.com/jslatts/nodechat with demo: nodechat.no.de
*
* Multiple Chat Room Example:
* *Answer:* https://github.com/Flotype/now/tree/master/examples/multiroomchat_example
* This looks like a powerful route to achieve what we are looking for with multiple room chat
* This one too: https://github.com/chrismatthieu/CHATS.iO // demo @ https://chats.io

## Some Initial Conclusions (MARKWK):
* After reviewing various nodejs chat resources, it seems that the best combination of technologies for nodejs chat with multiple room is: Node.JS, Express, Socket.io, NowJS, Redis
* NowJS
* The Multiroom chatroom example with NowJS offers a good start to what we want to achieve for multichatroom server. Extremely easy with the everyone.now function
* Not sure about handling permissions but this should be checked/handled on Drupal end. 
* *Questions*: How to handle chatroom db storage? redis? See this example https://github.com/jslatts/nodechat/
* It seems like it would be good to archive the chat sessions to drupal for obvious performance and backup reasons. So we'll need a way to pass a transcript of the conversation to Drupal. 

## Tasks:
1. Hack / build initial multichatroom server
2. Initial Module for adding chatroom integration as cck field for nodes
3. clarify Drupal calls according to chat server setup
4. Pulling General Chat into Drupal
* Pull Specific Chatroom into Drupal
* initial UI / chat embedding within Drupal node
* determine security considerations between chat server and drupal
* add drupal level security checks to only only certain users
* add level of security between chat sever and drupal 
* clean up UI / theming
* integrate with atrium_opentok to create seamless node.js and video chat 

===============================
# Developer Notes:
* Technologies: Node.JS, Express, Socket.io, NowJS (npm install now)

===============================
# Resources / Inspirations
* http://blip.tv/drupalcon/node_js-5493919
* http://nodetuts.com/
* http://fzysqr.com/2011/02/28/nodechat-js-using-node-js-backbone-js-socket-io-and-redis-to-make-a-real-time-chat-app/
* *Example*: https://github.com/bigbinary/node-chat-in-steps
* Docs for NowJS: http://nowjs.org/
* https://github.com/jslatts/nodechat and demo: nodechat.no.de
