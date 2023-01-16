# Fortigate CLI
Palomuurien komentorivien cheatsheet ja mitä jokaisen komennossa on tarkoituksena tehdä ja mitä tekee mitäkin

| Command | description | other |
| --------- | ---------- | ------- |
| <b> Configuration </b> | 
| check configuration	| # show <br> # show \| grep xxxx <br> # show full-configuration <br> #show full-configuration \|  grep XXXX <br> #show full-configuration \| grep -f XXXX ← display with tree view <br>
| --------- | ---------- | ------- |
| <b> Network </b> | ---------- | ------- |
| Check Routing	| # get router info routing-table detail <br> # show router static <br><br> #config router static <br> (static)# show <br> (static)# end <br> |
| Check Firewall Policy	| # show firewall policy <br> # show firewall policy XXXX <br><br> #config firewall policy <br> (policy)# show |
| --------- | ---------- | ------- |
| Check Hardware Information | # get hardware status |
| check Version, BIOS, Firmware, etc | # get system status |
| Display CPU / memory / line usage	 | # get system performance status |
| Display of NTP server	 | # get system ntp |
| Display the current time and the time of <br> synchronization with the NTP server | # execute time |
| check interfaces status , Up or Down | # get system interface physical |
| check interfaces | # config system interface <br> (interface)# show <br> (interface)# end |
| display of arp table | # get system arp |
| --------- | ---------- | ------- |
| HA (High Availability)| solution for providing redundancy |
| Check HA Status | # get system ha status |
| Check HA Configuration | # get system ha <br> #show system ha |
| --------- | ---------- | ------- |
| NTP (Network Time Protocol) | # execute time <br> #get system ntp <br> #diagnose sys ntp status |
| Check NTP	|  |
 --------- | ---------- | ------- |
| Set and change Examples |  |
| Save Configuration & exit	| (console) # end  |
| Don't Save Configuration & exit | (console) #abort |
|  |  |

## Määrityksiä 
Määrityksestä on mm. policy , operaattorit editointi tai poisto tai sen prosessointi

<b> Object operation </b>
#config firewall address <br>
(address) # show   <-- check all address configuration <br>
(address) # end <br><br>

#config firewall address <br>
(address) # edit "test1" <br>
(address) # show     <- check <br>
(address) # abort    <- End and discard last config <br><br>

#config firewall address <br>
(address) # edit "test1" <br>
(address) # show    <- check <br> 
(address) # set subnet 192.168.0.5 255.255.255.0 <br>
(address) # show   <- check <br>
(address) # end   <- End and save last config. <br><br>

config firewall address <br>
  edit "test-server-10" <br>
    set associated-interface "vlan10" <br>
    set subnet 192.168.0.5 255.255.255.0 <br>
end<br><br>

<br>
<b>Policy Operation</b>
<br>
#config firewall policy <br>
(policy)# show    <- show all policy  <br>
(policy)# end <br><br>


#config firewall policy <br>
(policy)# edit 555 <br>
(policy)# show <br>
(policy)# abort   <- End and discard last config <br><br>

config firewall policy <br>
  edit 555 <br>
    set name "test" <br>
    set srcintf "vlan10" <br>
    set dstintf "port 5" <br>
    set srcadr "xxxx"  "xxxx"  "xxx" <br>
    set action accept <br>
    set schedule "always" <br>
    set servie "HTTP" "ICMP_ANY" <br>
end    <- End and save last config. <br><br>

<br> 
<b> delete command </b> <br>
# config firwall policy <br>
# delete 1 <br>
# end <br>
<b>How to delete router</b> <br>
# config router static <br>
# delete 1 <br>
# end <br><br>

## Vahvistamiset
 
Fortigate vahvistamisen komennot <br>

| Help	| # ? | <br>
| ping	| # execute ping 192.168.0.1 | <br>
| traceroute | # execute traceroute 192.168.1.1 | <br>
| telnet | # execute telnet 192.168.0.10 <br> # execute telnet 192.168.0.1 22 | <br>
| ssh | # execute ssh user@192.168.0.10 <br> # execute ssh user@192.168.0.10 23 | <br>
| execute command like tcpdump | # diagnose sniffer packet port15 ← Interface Port15 <br> # diagnose sniffer packet any 'host xx.xx.xx.xx' <br> # diagnose sniffer packet port15 'host xx.xx.xx.xx' <br> # diagnose sniffer packet any 'host xx.xx.xx.xx or host yy.yy.yy.yy' <br> # diagnose sniffer packet any 'udp port 53 or tcp port 53' <br> # diagnose sniffer packet any 'host xx.xx.xx.xx and tcp port 80' <br> | <br>
| shutdown | # execute shutdown | <br>
| clear arp table | # execute clear system arp table | <br>
| --------- | ---------- | ------- | <br>
| <b> Backup Configuration <b> | # exec backup config tftp conf/test-fw-01_20180913.conf 192.168.0.10 | <br>
| <b> Displaying logs via CLI <b> |  | <br>
<b> Check log filter </b> <br>
#execute log filter dump <br>
category: traffic <br>
deice: memory <br>
(snipp) <br>
Filter: <br>
(snipp) <br>
<br>

<b>set filter</b>
# execute log filter device    <- Check Option
Example output (can be different if disk logging is available):
Available devices:
0: memory
1: disk
2: fortianalyzer
3: forticloud

#execute log filter device XX   <- Set Option

#execute log filter category    <- Check Option
 0: traffic
 1: event
 2: utm-virus
 3: utm-webfilter
 4: utm-ips
 5: utm-emailfilter
 7: utm-anomaly
 8: utm-voip
 9: utm-dlp
10: utm-app-ctrl
12: utm-waf
15: utm-dns
16: utm-ssh
17: utm-ssl
18: utm-cifs
19: utm-file-filter
#execute log filter category XXXX   <- Set Option
<br>

<b>Example</b>

#execute log filter device 1       <- 1: disk
#execute log filter category 1     <- 1: event

<b>View log</b>
#execute log display








