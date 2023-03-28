# Dynamic IP lists for Palo Alto

*WARNING: USE THIS REPO AT YOUR OWN RISK*
forked from *jtschichold/panwdbl-actions* All creds

## Details

- each range feed has a correspending Github Action workflow and a dedicated branch
- the workflows are triggered based on the schedule specified in each workflow YAML file
- each workflow:
    * checkouts the branch of the feed
    * grabs the original range feed
    * process the range: feed using a dedicated script contained in the branch
    * if there are changes, a commit & push is performed to update the repo contents

## Feeds

| Feed                                     | Description                                                       | URL                                                                                    |
|------------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| DShield Top 20                           | DShield.org Recommended Block List                                | https://raw.githubusercontent.com/K4S1/pan-dyn-lists/dshield/dshieldbl.txt             |
| Tor Exit Nodes                           | List of Tor Exit Nodes from https://www.dan.me.uk/tornodes        | https://raw.githubusercontent.com/K4S1/pan-dyn-lists/tor/exit-nodes.txt                |
| SSL Abuse IP List                        | SSLBL 30 days block list. See https://sslbl.abuse.ch/blacklist/   | https://raw.githubusercontent.com/K4S1/pan-dyn-lists/sslabuseiplist/sslabuseiplist.txt |
| Emerging Threats Known Compromised Hosts | See https://doc.emergingthreats.net/bin/view/Main/CompromisedHost | https://raw.githubusercontent.com/K4S1/pan-dyn-lists/etcompromised/etcompromised.txt   |
| MS365 Teams                              | Microsoft Teams IP ranges                                         | https://raw.githubusercontent.com/K4S1/pan-dyn-lists/ms365/Teams.txt                   |
| MS365 Exchange                           | Microsoft Exchange IP ranges                                      | https://raw.githubusercontent.com/K4S1/pan-dyn-lists/ms365/Exchange.txt                |


## Lists to be added Feeds

Some of the feeds that used to be available on pandwbl haven't be ported to this incarnation. Details below:

| Feed                | Description                                                                                                                                                                                                                        | URL                                                         | Notes                |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------|
| Spamhaus DROP       | DROP (Don't Route Or Peer) and EDROP are advisory "drop all traffic" lists, consisting of stolen 'hijacked' netblocks and netblocks controlled entirely by criminals and professional spammers. See http://www.spamhaus.org/drop/. | https://www.spamhaus.org/drop/drop.txt                      | Use the original URL |
| Spamhaus DROP       | DROP (Don't Route Or Peer) and EDROP are advisory "drop all traffic" lists, consisting of stolen 'hijacked' netblocks and netblocks controlled entirely by criminals and professional spammers. See http://www.spamhaus.org/drop/. | https://www.spamhaus.org/drop/edrop.txt                     | Use the original URL |
| BruteForceBlocker   | See http://danger.rulez.sk/index.php/bruteforceblocker/                                                                                                                                                                            | http://danger.rulez.sk/projects/bruteforceblocker/blist.php | Use the original URL |
| Malware Domain List | See http://www.malwaredomainlist.com/                                                                                                                                                                                              | http://www.malwaredomainlist.com/hostslist/ip.txt           | Seems inactive       |

