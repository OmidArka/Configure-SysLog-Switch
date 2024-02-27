# Configure-SysLog-Switch

R1# configure terminal
R1(config)# logging host x.x.x.x
R1(config)# logging trap informational (it differ on your requirement, choose between severity levels 0-7)
R1(config)# logging history informational (as above)
R1(config)# logging origin-id hostname
R1(config)# facility local6
R1(config)# logging host x.x.x.x transport udp port x
R1(config)#logging console
R1(config)#logging rate-limit console all except critical
R1(config)#logging source-interface Vlan 99
Additionally, it is worth using the following commands:
R1(config)# service sequence numbers
R1(config)# service timestamps log![image](https://github.com/OmidArka/Configure-SysLog-Switch/assets/153341501/c1d0ddb9-0513-4238-8e08-475685580f20)
