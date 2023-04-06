# Cisco 3600 switch

ESW1#show version
Cisco IOS Software, 3600 Software (C3640-IK9O3S-M), Version 12.4(25b), RELEASE SOFTWARE (fc1) <br>
Technical Support: http://www.cisco.com/techsupport <br>
Copyright (c) 1986-2009 by Cisco Systems, Inc. <br>
Compiled Wed 12-Aug-09 12:52 by prod_rel_team <br>
<hr>

Tänne tulee cisco 3600 kytkimiä ja ehkä mahdolliset cisco sarja tuoteitta ei vain 3600 tai 7200 sarja ja jne. sekä tarvittaessa muita reititimiä

* [cheat sheet commands](#cheat-sheet-commands)

## cheat sheet commands

ESW1#show ?
  aaa                       Show AAA values
  aal2                      Show commands for AAL2
  access-expression         List access expression
  access-lists              List access lists
  accounting                Accounting data for active sessions
  adjacency                 Adjacent nodes
  alarm-interface           Display information about a specific Alarm
                            Interface Card
  aliases                   Display alias commands
  alignment                 Show alignment information
  alps                      Alps information
  appfw                     Application Firewall information
  archive                   Archive of the running configuration information
  arp                       ARP table
  async                     Information on terminal lines used as router
                            interfaces
  auto                      Show Automation Template
  backhaul-session-manager  Backhaul Session Manager information
  backup                    Backup status
  bcm560x                   BCM560x HW Table
  bgp                       BGP information
  bridge                    Bridge Forwarding/Filtering Database [verbose]
  bsc                       BSC interface information
  bstun                     BSTUN interface information
  buffers                   Buffer pool statistics
  c3600                     Show c3600 information
  call                      Show call
  call-manager-fallback     Show call-manager fallback configuration & stats
  caller                    Display information about dialup connections
  cca                       CCA information
  ccm-manager               Call Manager Application information
  cdapi                     CDAPI information
  cdp                       CDP information
  cef                       Cisco Express Forwarding
  class-map                 Show QoS Class Map
  clns                      CLNS network information
  clock                     Display the system clock
  cls                       DLC user information
  cns                       CNS agents
  compress                  Show compression statistics
  configuration             Configuration details
  connection                Show Connection
  context                   Show context information about recent crash(s)
  controllers               Interface controller status
  cops                      COPS information
  credentials               Show credentials service configuration
  crm                       Carrier Resource Manager info
  crypto                    Encryption module
  dampening                 Display dampening information
  data-corruption           Show data errors
  debugging                 State of each debugging option
  derived-config            Derived operating configuration
  dhcp                      Dynamic Host Configuration Protocol status
  diag                      Show diagnostic information for port
                            adapters/modules
  dial-peer                 Dial Plan Mapping Table for, e.g. VoIP Peers
  dialer                    Dialer parameters and statistics
  dialplan                  Voice telephony dial plan
  diffserv                  Differentiated services
  dlsw                      Data Link Switching information
  dnsix                     Shows Dnsix/DMDP information
  dot1x                     IEEE 802.1X
  drip                      DRiP DB
  dspfarm                   Display DSPFARM related information
  dspu                      Display DSPU information
  dss                       DSS information
  dtp                       DTP information
  dxi                       atm-dxi information
  echo-cancel               Show Echo-cancellation Info
  entry                     Queued terminal entries
  environment               Environmental monitor statistics
  eou                       EAPoUDP
  ephone                    Show all or one ephone status
  ephone-dn                 Show all or one IP phone line
  ephone-hunt               Show all or one hunt group
  errdisable                Error disable
  etherchannel              EtherChannel information
  event                     Embedded event related commands
  event-manager             Event manager information
  exception                 exception information
  fb-its-log                Call-Manager-Fallback or IP Telephony Service Log
  file                      Show filesystem information
  flash:                    display information about flash: file system
  flow-sampler              Display the flow samplers configured
  frame-relay               Frame-Relay information
  fras                      FRAS Information
  fras-host                 FRAS Host Information
  funi                      FUNI information
  gateway                   Show status of gateway
  glbp                      GLBP information
  h323                      Show H.323 VoIP information
  hardware                  Hardware specific information
  history                   Display the session command history
  hosts                     IP domain-name, lookup style, nameservers, and host
                            table
  html                      HTML helper commands
  http                      Display HTTP info
  idb                       List of Interface Descriptor Blocks
  interfaces                Interface status and configuration
  inventory                 Show the physical inventory
  ip                        IP information
  ipv6                      IPv6 information
  isis                      IS-IS routing information
  iua                       ISDN User Adaptation Layer information
  key                       Key information
  kron                      Kron Subsystem
  l2cac                     L2 CAC
  l2tun                     Layer 2 tunnel information
  lat                       DEC LAT information
  line                      TTY line information
  llc2                      IBM LLC2 circuit information
  local-ack                 Local Acknowledgement virtual circuits
  location                  Display the system location
  logging                   Show the contents of logging buffers
  login                     Display Secure Login Configurations and State
  mac-address-table         MAC forwarding table
  management                Display the management applications
  memory                    Memory statistics
  mgcp                      Display Media Gateway Control Protocol information
  microcode                 show configured microcode for downloadable hardware
  mls                       multilayer switching information
  modem                     Show modem
  modemcap                  Show Modem Capabilities database
  monitor                   Monitoring different system events
  mpoa                      MPOA show commands
  mrcp                      MRCP information
  mwi                       mwi related information
  ncia                      Native Client Interface Architecture
  netbios-cache             NetBIOS name cache contents
  node                      Show known LAT nodes
  ntp                       Network time protocol
  num-exp                   Number Expansion (Speed Dial) information
  oer                       Optimized Exit Routing information
  pagp                      Port channel information
  parser                    Display parser information
  pas                       Port Adaptor Information
  pci                       PCI Information
  pm                        Show Port Manager commands
  policy-manager            Policy Manager
  policy-map                Show QoS Policy Map
  ppp                       PPP parameters and statistics
  pppatm                    PPP over ATM
  pppoe                     PPPoE information
  printers                  Show LPD printer information
  privilege                 Show current privilege level
  processes                 Active process statistics
  protocols                 Active network routing protocols
  qdm                       Show information about QoS Device Manager
  qllc                      Display qllc-llc2 and qllc-sdlc conversion
                            information
  queue                     Show queue contents
  queueing                  Show queueing configuration
  radius                    Shows radius information
  random-detect-group       display random-detect group
  rbscp                     RBSCP information
  region                    Region Manager Status
  registry                  Function registry information
  reload                    Scheduled reload information
  resource                  Display Resource Usage/Relations and more details
  rhosts                    Remote-host+user equivalences
  rif                       RIF cache entries
  rmi                       Resource User Infrastructure information
  rmon                      rmon statistics
  route-map                 route-map information
  rpms-proc                 RPMS Process Information
  rtpspi                    RTP Service Provider Interface
  rtsp                      Real Time Streaming Protocol information
  rudpv1                    Rudpv1 information
  running-config            Current operating configuration
  sccp                      Display Skinny Client Control Protocol information
  scp                       SCP commands
  sdllc                     Display sdlc - llc2 conversion information
  sdspfarm                  Show dspfarm status from SCCP server
  services                  LAT learned services
  sessions                  Information about Telnet connections
  settlement                Show status of settlement
  sgbp                      SGBP group information
  sip-ua                    Show SIP User Agent
  slm                       XML data structure information
  slot0:                    display information about slot0: file system
  slot1:                    display information about slot1: file system
  smf                       Software MAC filter
  sna                       Display SNA host information
  snapshot                  Snapshot parameters and statistics
  snmp                      snmp statistics
  source-bridge             Source-bridge parameters and statistics
  spanning-tree             Spanning tree topology
  srcp                      Display SRCP Protocol information
  ssh                       Status of SSH server connections
  ssl                       Show SSL command
  sss                       SSS Information
  stacks                    Process stack utilization
  standby                   Hot Standby Router Protocol (HSRP) information
  startup-config            Contents of startup configuration
  storm-control             Show packet storm control configuration
  stun                      STUN status and configuration
  subscriber-policy         Subscriber policy
  subscription              Subscription information to show
  subsys                    Show subsystem information
  table-map                 Show Table Map
  tacacs                    Shows tacacs+ server statistics
  tbct                      Show TBCT related parameters
  tcp                       Status of TCP connections
  tdm                       TDM connection information
  tech-support              Show system information for Tech-Support
  telephony-service         Show Cisco IOS Telephony Service Configuration &
                            Stats
  template                  Template information
  terminal                  Display terminal configuration parameters
  tgrep                     Show TGREP information
  time-range                Time range
  track                     Tracking information
  traffic-shape             traffic rate shaping configuration
  translate                 Protocol translation information
  translation-rule          Show translation rule table
  trunk                     Trunk Group info
  tunnel                    Show configured tunnels
  users                     Display information about terminal lines
  vc-group                  Show VC Group
  version                   System hardware and software status
  vlan-range                VLAN Range
  vlan-switch               VTP VLAN status
  vlans                     Virtual LANs Information
  voice                     Voice port configuration & stats
  voip                      Voice over Internet Protocol information
  vpdn                      VPDN information
  vrrp                      VRRP information
  vsp                       Voice Streaming Processing information
  vtemplate                 Virtual Template interface information
