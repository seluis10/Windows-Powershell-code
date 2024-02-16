# Import the Active Directory
Import-Module ActiveDirectory 

# Set variables outside the loop
$baseComputerName = "Win10-"
$containerDN = "CN=Computers,DC=exampledomain,DC=com"  # Actual container DN

# Use a loop for generating sequential numbers
$computerNames = 1..100 | ForEach-Object { "$baseComputerName$_" }

# Create computer accounts in a single batch
New-ADComputer -Name $computerNames -Path $containerDN -SamAccountName $computerNames -Enabled $true

# Output message
Write-Host "Created 100 computer accounts: $computerNames"
