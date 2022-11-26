## AUTHENICATION (s129)
## 0x00 STRING
#
## Message (s129)
## 0x01 STRING
#
## JOIN (s129)
## 0x02 STRING
#
## LEAVE (s129)
## 0x03 STRING
#
## USERNAME CHANGE (s257)
## 0x04 STRING STRING
#
## types
## Strings - ASCII padded 128 char with 0x20
#

## authenication system
1. User connects with unique IP
2. Is given a unique token which is linked with their IP and useranme
and other data, and also unique ID which the server can identifiy player's by (and clients, would need protocol changes however probably everywhere)
3. The client then stores this token, and uses it to log into the server with the authenication packet and the token

