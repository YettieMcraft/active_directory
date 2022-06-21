# Install Domain Controller

1. Use 'sconfig' to change hostname
    - 8 for network settings
    - change ip address to static but end with .155
    - subnet mask default, use default gateway ending in .2
    - change the DNS server to our own ip address

2. set up remote
    - use set-item wsman:/localhost/Client/TrustedHosts -value <ip ending in 155>
    - connect using Enter-PSSession <ip> -Credential (Get-Credential)

2. Install active directory windows feature

shell: Install-WindowsFeature AD-Domain-Services -IncludeManagementTools