# Dedication server commands

Command Line Arguments list for dedication there are:

*   \-gameServerStart : Start dedicate server
*   \-gameServerPort : Change server port
*   \-gameMaxConnections : Max server connections
*   \-gameOnlineScene : Scene name which players will join for the battle
*   \-gameRule : Name of game rule, for the demo there are IONetworkGameRule, DeathMatchNetworkGameRule
*   \-gameBotCount : Amount of bots

Example of command line usage (For Linux/Mac)

> ./Build.x86\_64 -gameServerStart -gameServerPort 7700 -gameMaxConnections 50 -gameOnlineScene "Battle" -gameRule "IONetworkGameRule" -gameBotCount 10

For Windows you can set arguments in shortcut’s properties

![](../images/1KJWv-ACSU1IOT_h7wmRCWA.png)

So by this example, server configurations will be set as:

*   Server Port = 7700
*   Max Connections = 50
*   Online Scene = Battle
*   Game Rule = IONetworkGameRule
*   Bot Count = 10

* * *

### How to make connection to server button example

Select the button you want to use it to connect to your server , for this example I will use PlayOnlineButton

Then add button on click event to set Network Address, Network Port and start server

![](../images/1jNAS7z8hOGdg4rfXORubLQ.png)

![](../images/1UwvWK95ZY-btHR5RhcasOg.png)

![](../images/1bJLFYZHTf6ZYzGCHIZZEAg.png)

![](../images/1BiBr8OSd26Q65T8Kr4PfJA.png)