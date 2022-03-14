# probable-octo-journey
bannanas
cheesse

Version TAG 6

Amiga 1000

atari st 1020
chase
*This text is italicized*

hello there
- this is a test 1
- this next test 2
- well on test 3

  
  | Value | Option        |
  |-------|---------------|
  | 1     | Slack         |
  | 2     | eMail         |
  | 4     | Console       |
  | 8     | File          |
  | 16    | Telegram      |
  | 32    | Nextcloud     |
  
<details><summary>ComputerSayz</summary>
  
  Hello there peoplez
  
  </details>
   
## Commands
`bash
cloudflare-template.sh -help` 

`bash cloudflare-template.sh -tolerant mydomain.com -sleep=10 example.com -proxy=false www.example.com -auth_ttl=10 x1.example.com`

<details><summary>[script] -help, -tolerant, -debug, -config_file, -sleep, -rsleep, -purge</summary>
  
- -help , list commands
  
- -tolerant ,  - - - - - - TODO - - - - -

- -debug , will output to console a debug log
  
- -config_file=X , this is config that to used

- -sleep=X , this is sleep timer for that script

- -rsleep=X , this will set a random legth time sleep timer for the script
  
- <-details><-summary>-purge=x , To purge settings (operates using bitwise values)<-/summary>

</details>
  
<details><summary>[Cloudflare] -auth_email, -auth_method, -auth_key, -zone_identifier, -auth_ttl, -auth_proxy</summary>

-  -auth_email=X , The e-mail that used to login to cloudflare 'https://dash.cloudflare.com'

-  -auth_method=X , Set to "global" for Global API Key or "token" for Scoped API Token 
  
-  -auth_key=X , The Global API Key or Scope API Token
  
-  -zone_identifier=X , Can be found in the "Overview" tab of your domain
  
-  -auth_ttl=X DNS Record TTL (seconds)
  
-  -auth_proxy=X , Set to "ture" to using cloudflare Proxing service or set to "false" do disclose you IP publicly
  
</details>

<details><summary>[DNS] -record_name, -ip_recheck, -ip_set, -ip_maxage</summary>
  
- -record_name=X , this record that wish update [testing123.example.com]
  
- -ip_recheck , this will purge ip that know to system so will check if there updated one
  
- -ip_set=X ,  this will set ip record to what you want to define [1.1.1.1]. There 24 hours (86400 seconds) from time it set until recheck publicly for IP. _-ip_maxage_ value it upon this value, so if _-ip_maxage=60_ then is 24 hours and 1 minute (86460 seconds). If _-ip_recheck_ XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
  
- -ip_maxage=X , How many time (seconds) that have to pass until it checks for IP number again. If use _-ip_set_ then note changes that happen when using command _-ip_set_ for more information

</details>

<details><summary>[Reports] -report_distribution, -report_attribute, -report_name</summary>

  
- <details><summary>-report_distribution=X , services that being used sending reports (operates using bitwise values)</summary>
  
  
  | Value | Option        |
  |-------|---------------|
  | 1     | Slack         |
  | 2     | eMail         |
  | 4     | Console       |
  | 8     | File          |
  | 16    | Telegram      |
  | 32    | Nextcloud     |
   
  _example:_ 
    - Distribution **disable** set it to **0**. 
    
    - Distribution **Console** only set it to **4** (4=4). 
    
    - Distribution **eMail** and **Console** set it to **6** (2+4=6)
  
  </details>
- <details><summary>-report_attribute=X , control which atttibute is contained in the report (operates using bitwise values)</summary>
    
    
  | Value | Option        |
  |-------|---------------|
  | 1     | Account       |
  | 2     | Type          |
  | 4     | IP Address    |
  | 8     | Proxy         |
  | 16    | TTL           |
  | 32    | Time          |
  | 64    | Identifier    |
  | 128   | BootID        |
  | 256   | Status        |
  
  _example:_ 
    - Attribute **disable** set it to **0**.
    
    - Attribute **Account** only set it to **1**. 
    
    - Attribute **Account** and **Proxy** set it to **9** (1+8=9). 
    
    - Attribute **Acount**, **Type**, **IP Address**, **Proxy**, **TTL**, **Time**, **Identifier**, **BootID** and **Status** set it to **511** (1+2+4+8+16+32+64+128+256=511)
  
  
  </details>
  
- -report_name=X , this is system identifier name being used, if it not be set it will hostname instead

</details>

<details><summary>[Slack] -slackuri</summary>
  
  The _-report_distribution_ has an bitwise value of _1_
  
-  -slackuri=X , URI for Slack WebHook [https://hooks.slack.com/services/xxxxx]
  
  | Command              | Requirements |
  |----------------------|--------------|
  | -slackuri            | **Required** |
  
</details>

<details><summary>[SMTP] -email_username, -email_password, -email_smtp, -email_port, -email_fromName, -email_toName, -email_fromAddress, -email_toAddress</summary>

  The _-message_type_ has an bitwise value of _2_
  
-  -email_username=X , SMTP login username

-  -email_password=X , SMTP login password
  
-  -email_smtp=X , ip/domain name of the SMTP server
  
-  -email_port=X , port number used to connect to SMTP server
  
-  -email_fromName=X , name that being used for that e-mail (from) [Joe Bloggs]
  
-  -email_toName=X , name that being used for that e-mail (to) e-mail [Jane Doe]
  
-  -email_fromAddress=X , email address that being used (from) [joe@example.com]

-  -email_toAddress=X , email address that being used (to) [jane@example.org]
  
  | Command              | Requirements |
  |----------------------|--------------|
  | -email_username      | **Required** |
  | -email_password      | **Required** |
  | -email_smtp          | **Required** |
  | -email_port          | Recommended  |
  | -email_fromName      | Optional     |
  | -email_toName        | Optional     |
  | -email_fromAddress   | **Required** |
  | -email_toAddress     | Recommended  |
  
</details>

<details><summary>[File] -file_logPath</summary>
  
  The _-report_distribution_ has an bitwise value of _4_
 
-  -file_logPath=X , The location of where log file is saved
  
  | Command              | Requirements |
  |----------------------|--------------|
  | -file_logPath        | **Required** |
  
</details>


<details><summary>[Console] < No commands > </summary>
 
  The _-report_distribution_ has an bitwise value of _8_
  
  Output to Bash console
  
</details>

<details><summary>[Telegram] -telegram_token, -telegram_chatID</summary>
   
  The _-report_distribution_ has an bitwise value of _16_
  
-  -telegram_token=X , The API token that was issued by Telegram BotFather
  
-  -telegram_chatID=X , This is user that sending message to
  
  | Command              | Requirements |
  |----------------------|--------------|
  | -telegram_token      | **Required** |
  | -telegram_chatID     | **Required** |
  
  </details>
  
  <details><summary>[Nextcloud] -nextcloud_domain, -nextcloud_username, -nextcloud_apppass, -nextcloud_roomtoken</summary>
 
  The _-report_distribution_ has an bitwise value of _32_
  
-  -nextcloud_domain=X , The location of server as domain name [https://nextcloud.example.com] or as ip [https://192.168.1.60]
  
-  -nextcloud_username=X , The username name for Nextcloud
  
-  -nextcloud_apppass=X , The App-Password for Nextcloud
  
-  -nextcloud_roomtoken=X , Nexcloud talk room token ID
  
  | Command              | Requirements |
  |----------------------|--------------|
  | -nextcloud_domain    | **Required** |
  | -nextcloud_username  | **Required** |
  | -nextcloud_apppass   | **Required** |
  | -nextcloud_roomtoken | **Required** |
  
  </details>
