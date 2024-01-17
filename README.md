# S~~ANS~~ Holiday-Hack-Challenge-2023
 
<img width="800" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/d051e195-083b-431e-903d-cc42be8bcb79">  

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
To win the game we have to defeat elves and the Santa but boy is it difficult. As the hint says we need a powerful player to team with us and defeat elves and santa, that would be the Dwarf. Hint is in the Javascript source code of the game as highlighted below.

### Code Analysis:
The code appears to introduce a character (Elf the dwarf, jokingly referred to as Jared) into the game when in single-player mode.First, a sound effect named 'elf_the_dwarf_is_here' is played if audio is enabled. Next, a toast message appears on the screen saying "Elf the dwarf has joined your team!" for a short duration. Finally, a new game sprite named 'jaredSprite' is created at a specific position. All indicating we need the Dwarf.

View the source code of the game 
<img width="739" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/53a6d875-2c45-47e0-bf53-4788b72f4158">

```
 // Check if it's single-player mode
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

2. Choose play game with random players and once the game room to loads check the current loaded URL "window.location.href"
   
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

<details>
<summary>Solution</summary>
Noel Boetie used ChatNPT to write a pentest report. Go to Christmas Island and help him clean it up.
Reportinator

We are presented with a report to check if the vulnerabilities reported are true or false.
It is good to read through the report and get your answers but there is also an alternative way to do this challenege.

### Technique
There is a POST request with payload data for the 9 questions asked where 1 indicates false and 0 indicates true. With the help of Burpsuite we will first intercept the request and then pass it over to Intruder which would help with all the probable combinations for the correct answer.

#### Steps
1. Load the reportinator webpage and click on submit review directly. You will observe a POST request sent to https://hhc23-reportinator-dot-holidayhack2023.ue.r.appspot.com/check as below

   <img width="359" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/9b70534a-2edc-4f71-af70-a0d7e33613fa">

2. Add payload marker to the value of the parameter input as below. Choose Clusterbomb attack [Check all permutation of payload combination] now fill all the 9 payload set with our combination of 0 and 1.

   <img width="506" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/022888ba-fe19-4c1c-b5bd-8cab0e0021fb">

3. Lauch the attack and observe one response will have 200 response status code.

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
${\color{green}Great,/you/did/it/all!}$
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

This task introduces us to JWT token, how to decode/modify and work with modified token. Similar to previous tasks such as snowball fight the solution has to be worked on the same tab. There is a shortcut and an intended way to do this task. let's discuss both.



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
7. Upon wining the challenge we get below note which belongs to Alabaster Snowball 
   
   <img width="339" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/81cf67de-301f-4db7-b3ee-d308474ab458">

## Alternative Way

On the source code of the elf challenge we can see that there is a variable called score. If the score is 75 or higher, it updates the sessionJWT and stores it in a cookie. It pauses the game scene. So let's set the score as 80 and we win the game.

<img width="834" alt="image" src="https://github.com/Miragle-Hub/Holiday-Hack-Challenge-2023---SANS/assets/128744976/3537280c-5134-4f16-b28c-049f4121b315">



</details>

### Certificate SSHenanigans
Difficulty: 🎄🎄🎄🎄🎄

Go to Pixel Island and review Alabaster Snowball's new SSH certificate configuration and Azure [Function App](https://northpole-ssh-certs-fa.azurewebsites.net/api/create-cert?code=candy-cane-twirl) . What type of cookie cache is Alabaster planning to implement?


    

  












