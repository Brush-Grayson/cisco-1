<h1>Version Control Setup</h1>
<h2>Command modes</h2>
<h3>User Exec mode</h4>
    <p>
    Access to limited number of basic monitoring commands. <br> - Switch> <br> - Router> <br> 
    </p>
<h3>Privileged Exec Mode</h3>
    <p>
    Allows Access to all commands and features. <br> - Switch# <br> - Router#
    </p>
<h2>Navigation</h2>
    <p>- Switch>en to get to Priviliege mode <br> - Switch#disable to get to user mode 
    </p>
<h4>Line subconfiguration</h4> 
    <p>Switch(config)# line console 0 <br> Switch(config-line)# exit <br> Switch(config)#
    </p>
<h4>To move from any subconfiguration mode to the privileged exec mode</h4>
    <p> Switch(config-line)# end <br> Switch# </p>
<h4>Move from one subconfiguration mode to another</h4>
    <p>Switch(config-line)# interface FastEthernet 0/1 <br> Switch(config-if)#
    </p>
<h2>Hot keys/Shortcuts</h2>
    <p>- Tab: Completes partial command entry <br>- ?: Gives a built in guide. Ex> set clock ? <br> - Enter key: Displays next line <br>- Space: Next screen <br> - Ctrl-C: Ends configuration mode and returns to priviliged exec mode <br> - Ctrl-Z: Ends the configuration mode and returns to privilieged exec mode
    </p>
<h2>Device Names</h2>
    <p>Switch# configure terminal <br> Switch(config)# hostname Sw-Floor-1 <br> Sw-Floor-1(config)#
    </p>
<h2>Configure Passwords</h2>
    <p>Sw-Floor-1# configure terminal <br> Sw-Floor-1(config)# line console 0 <br>Sw-Floor-1(config-line)# password {password} <br>Sw-Floor-1(config-line)# login<br>Sw-Floor-1(config-line)#end <br> Sw-Floor-1#
    </p>
<h4>To secure Privileged EXEC access</h4>
    <p> - Sw-Floor-1# configure terminal <br> - Sw-Floor-1(config)# enable secret {password} <br> - Sw-Floor-1(config)# exit <br> - Sw-Floor-1#
    </p>
<h4>Virtual terminal (VTY) Lines</h4>
    <p>Sw-Floor-1# configure terminal <br> Sw-Floor-1 (config)# line vty 0 15 <br> Sw-Floor-1(config-line)# password {password} <br> 
    Sw-Floor-1(config-line)# login <br> Sw-Floor-1(config-line)# end <br> Sw-Floor-1#
    </p>
<h4>Encryption</h4>
    <p> Sw-Floor-1# configure terminal <br> Sw-Floor-1(config)# service password-encryption <br> Sw-Floor-1# <br> Show running-config: Sw-Floor-1# show running-config
    </p>
<h4>Banner Messages</h4>
    <p>Sw-Floor-1# configure terminal <br> Sw-Floor-1(config)# banner motd #Authorized Access Only#
    </p>
<h2>Configure IP Addressing</h2>
    <p>View Network connections IpV4 <br> - Use following IP address </p>
    <p>SVI Configuration <br> Sw-Floor-1# configure terminal <br> Sw-Floor-1(config)# interface vlan 1 <br> Sw-Floor-1(config-if)# ip address 192.168.1.20 255.255.255.0 <br>Sw-Floor-1(config-if)# no shutdown <br> Sw-Floor-1(config-if)# exit <br> Sw-Floor-1(config)# ip default-gateway 192.168.1.1 - not needed
    </p>
<h4>Verify Connectivity in cmd</h4>
    <p> - >ping 192.168.1.2 <br> - >ping Sw-Floor-1 <br> Ping both switches and IP's
    </p>
<h4>Verify the IP address config on S1+S2</h4>
    <p>- show ipinterface brief</p>
<h3>SAVE CONFIGURATIONS: COPY RUN START
    