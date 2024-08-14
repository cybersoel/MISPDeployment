<h1 align="center">Summary Diagram</h1>


<p align="center">
<br/>
<img width="780" alt="Portfolio" src="https://i.imgur.com/HypVCz8.png">
<br />
</p>




<br />
<br />

<h1 align="center">Project walk-through</h1>

<br />
<br />

---
<a name="toc"></a>
**Table of Contents:**

- 


---

<h4>Tip: Any configuration options not mentioned in the walkthrough can be left at their default settings</h4>

---
## Downloading MISP

<br />
<br />


 - Navigate to misp-project.org/download/ and scroll down to the "Virtual image for testing" section.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/TuuFlxt.png">
<br />
<br />
<br />
<br />


 - Download the latest version of the .ova file. This file contains a pre-configured MISP virtual machine.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/RKkaHrt.png">
<br />
<br />
<br />
<br />


 - Once the download is complete, open Oracle VirtualBox. Go to File > Import Appliance.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/IbuzUqA.png">
<br />
<br />
<br />
<br />




 - Click "Next" to proceed with the import process.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/CXCXzxO.png">
<br />
<br />
<br />
<br />


 - Leave the default settings as they are and click "Finish" to deploy the virtual machine (VM).

<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/3kfRRFX.png">
<br />
<br />
<br />
<br />

 - After the import finishes, run the VM.

<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/iqFVfar.png">
<br />
<br />
<br />
<br />


 - Log in using the username "misp" and password "Password1234".
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/bechinE.png">
<br />
<br />
<br />
<br />



 - Try running the command `ifconfig`. You'll see the message `Command 'ifconfig' not found`
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/RpmtjDV.png">
<br />
<br />
<br />
<br />


 - Install the necessary networking tools by running: `sudo apt install net-tools`
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/CAVadbX.png">
<br />
<br />
<br />
<br />



 - To ensure your VM has its own unique IP address, go to [Machine] > [Settings] > [Network] and change "Attached to" to "Bridged Adapter".
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/543H3Rm.png">
<br />
<br />
<br />
<br />


 - Restart the VM and run "ifconfig" again. You should now see the VM's unique IP address (e.g., 192.168.1.63).
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/a0l6goP.png">
<br />
<br />
<br />
<br />



 - Configure the MISP baseurl to use the VM's IP address: Run `sudo /var/www/MISP/app/Console/cake admin setSetting MISP.baseurl https://[yourIPaddress]`
 - Verify the configuration: `grep baseurl /var/www/MISP/app/Config/config.php`

<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/CsRomkV.png">
<br />
<br />
<br />
<br />


 - On your host machine, open a web browser and navigate to the MISP interface. Log in with admin@admin.test (password: admin). You'll be prompted to change your password.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/1rVPuI2.png">
<br />
<br />
<br />
<br />

 - You can now explore the MISP interface.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/5kwVmfM.png">
<br />
<br />
<br />
<br />


 - Verify your baseurl setting in [Server Setting & Maintenance] > [MISP settings]
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/gBn0ECz.png">
<br />
<br />
<br />
<br />



 - Go to List Users to see that you're currently the only user.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/BDl0CoK.png">
<br />
<br />
<br />
<br />

 - Check your permissions in User settings.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/5pVt6cJ.png">
<br />
<br />
<br />
<br />


 - Add a new user: Go to Add User, set up an email and organization, then click Create user.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/31LEZDn.png">
<br />
<br />
<br />
<br />

 - Confirm that the new user (e.g., test@test.com) has been added successfully.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/TsoJfsU.png">
<br />
<br />
<br />
<br />


 - Go to [Administration] > [List Organizations] to view existing organizations.

<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/F14h9Au.png">
<br />
<br />
<br />
<br />

 - Edit the default "ORGNAME" organization (e.g., "Soel_Lab_BlueTeam") by clicking on it and selecting "Edit Organization".
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/HGbQBN3.png">
<br />
<br />
<br />
<br />


 - Add a new organization (e.g., "Soel_Lab_RedTeam") for demonstration purposes.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/Wbj9MYv.png">
<br />
<br />
<br />
<br />






23
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/lwDNBip.png">
<br />
<br />
<br />
<br />






24
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/f56vsuO.png">
<br />
<br />
<br />
<br />






25
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/juzItA3.png">
<br />
<br />
<br />
<br />






26
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/PRFPJlp.png">
<br />
<br />
<br />
<br />






27
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/FLyekhs.png">
<br />
<br />
<br />
<br />






28
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/CJ67kq8.png">
<br />
<br />
<br />
<br />






29
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/ZMLBVIQ.png">
<br />
<br />
<br />
<br />






30
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/5mrGpfT.png">
<br />
<br />
<br />
<br />






31
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/TIc7QMz.png">
<br />
<br />
<br />
<br />






32
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/WkxGmR5.png">
<br />
<br />
<br />
<br />






33
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/GAopKRF.png">
<br />
<br />
<br />
<br />






34
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/ANy1fxq.png">
<br />
<br />
<br />
<br />






35
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/jqrtDeg.png">
<br />
<br />
<br />
<br />






36
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/ZsGpEsM.png">
<br />
<br />
<br />
<br />






37
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/v4ITOE8.png">
<br />
<br />
<br />
<br />






38
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/5giynmX.png">
<br />
<br />
<br />
<br />






39
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/tZadfIv.png">
<br />
<br />
<br />
<br />






40
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/rpRvuq9.png">
<br />
<br />
<br />
<br />






41
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/dQBsYJs.png">
<br />
<br />
<br />
<br />






42
<p align="center">
<br/>
<img width="410" alt="Portfolio" src="https://i.imgur.com/JdtpUgh.png">
<br />
<br />
<br />
<br />






43
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/FGJntVw.png">
<br />
<br />
<br />
<br />






44
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/i0Kyq9C.png">
<br />
<br />
<br />
<br />






45
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/hbkp0FC.png">
<br />
<br />
<br />
<br />






46
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/AAM6qjo.png">
<br />
<br />
<br />
<br />






47
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/4GKKOSB.png">
<br />
<br />
<br />
<br />






48
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/AK1KKwC.png">
<br />
<br />
<br />
<br />






49
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/Xq0tfPR.png">
<br />
<br />
<br />
<br />






50
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/B8JrXoC.png">
<br />
<br />
<br />
<br />






51
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/pa01aHy.png">
<br />
<br />
<br />
<br />






52
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/y3dKgw9.png">
<br />
<br />
<br />
<br />






53
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/6opi8vM.png">
<br />
<br />
<br />
<br />






54
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/sN5NoVl.png">
<br />
<br />
<br />
<br />



55
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/zgC1ueH.png">
<br />
<br />
<br />
<br />


56
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/HkqQWOk.png">
<br />
<br />
<br />
<br />

57
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/AxgGNBU.png">
<br />
<br />
<br />
<br />





\<end\>

[back to top](#toc)

<br />
<br />
<br />

