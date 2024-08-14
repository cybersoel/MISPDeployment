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


---
## Importing and Running on VirtualBox 

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

---
## Initial MISP Configuration

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


---
## Accessing MISP Web Interface


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

---
## User Management


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

---
## Organization Management



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



 - Move the new user to the Red Team organization by editing their user profile.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/lwDNBip.png">
<br />
<br />
<br />
<br />

---
# Customizing the Dashboard 

 - Explore the Dashboard, where you can add widgets to monitor various aspects of the platform.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/f56vsuO.png">
<br />
<br />
<br />
<br />




 - First, let's add a widget for MISP workers. Click [Add Widget]. Pick [MISP Workers] and Submit
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/juzItA3.png">
<br />
<br />
<br />
<br />


 - The MISP Workers widget is now added to your dashboard. This widget displays the running processes for the backend, with workers designed for different tasks.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/PRFPJlp.png">
<br />
<br />
<br />
<br />



 - Add another widget for trending tags, which will be automatically populated when we import intelligence later.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/FLyekhs.png">
<br />
<br />
<br />
<br />

---
## Importing Threat Feeds

 - Navigate to Sync Actions - List Feeds.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/CJ67kq8.png">
<br />
<br />
<br />
<br />


 - You should see numerous default feeds. If the list is empty, click "Load default threat feed metadata".
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/ZMLBVIQ.png">
<br />
<br />
<br />
<br />


 - Enable the first five feeds in the list.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/5mrGpfT.png">
<br />
<br />
<br />
<br />


 - Using the down-arrow icon on the right of each feed, pull all events for the first three feeds.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/TIc7QMz.png">
<br />
<br />
<br />
<br />

---
## Managing MISP Workers 


 - Return to the Dashboard. You should now see three pending jobs. If no workers appear alive in your MISP workers widget, you can initialize them from the VM.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/WkxGmR5.png">
<br />
<br />
<br />
<br />



 - In the VM terminal, run the command: `sudo -u www.data bash /var/www/MISP/app/Console/worker/start.sh`
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/GAopKRF.png">
<br />
<br />
<br />
<br />


 - You can also manage workers from the web interface under Administration - Server Setting & Maintenance. Your Dashboard should now show workers as alive and processing the events.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/ANy1fxq.png">
<br />
<br />
<br />
<br />


---
## Exploring Imported Events



 - Go to Event Action - List Event to view the imported intelligence.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/jqrtDeg.png">
<br />
<br />
<br />
<br />


 - Click the eye icon next to an event to view its details.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/ZsGpEsM.png">
<br />
<br />
<br />
<br />


 - Examine a ransomware event. It also shows the publisher (e.g., CIRCL, the developer of MISP) and various assigned tags.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/v4ITOE8.png">
<br />
<br />
<br />
<br />



 - Scroll to the bottom of the event page to see all types of Indicators of Compromise (IOCs).
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/5giynmX.png">
<br />
<br />
<br />
<br />



 - Look for external links, such as a VirusTotal link, which may be included in the event.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/tZadfIv.png">
<br />
<br />
<br />
<br />



 - If available, follow the VirusTotal link to see additional information about the malware.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/rpRvuq9.png">
<br />
<br />
<br />
<br />


---
## Analyzing Events with MITRE ATT&CK


 - Return to the event list and select another example to examine.

<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/dQBsYJs.png">
<br />
<br />
<br />
<br />


 - In this new event, you may find numerous MITRE ATT&CK tactics mapped.
<p align="center">
<br/>
<img width="410" alt="Portfolio" src="https://i.imgur.com/JdtpUgh.png">
<br />
<br />
<br />
<br />



 - Scroll to the bottom of this event to view its associated IOCs.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/FGJntVw.png">
<br />
<br />
<br />
<br />


 - Return to the top of the event page and click on "Attack Matrix".

<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/i0Kyq9C.png">
<br />
<br />
<br />
<br />


 - Observe the MITRE ATT&CK matrix showing which tactics have been mapped to this event, allowing you to track the threat actor's activity.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/hbkp0FC.png">
<br />
<br />
<br />
<br />

---
## Creating a Custom Event



 - To add your own event, click "Add Event".

<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/AAM6qjo.png">
<br />
<br />
<br />
<br />


 - Name the event "APT28 NCSC REPORT", set the Threat Level to "Undefined", and set Distribution to "your organization only". Click submit.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/4GKKOSB.png">
<br />
<br />
<br />
<br />


 - In a new browser tab, navigate to ncsc.gov.uk/news/indicators-of-compromise-for-malware-used-by-apt28
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/AK1KKwC.png">
<br />
<br />
<br />
<br />



 - Locate and copy the list of IOCs from the NCSC (National Cyber Security Centre) report on APT28.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/Xq0tfPR.png">
<br />
<br />
<br />
<br />


 - Back in MISP, click the freetext import tool within your new event.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/B8JrXoC.png">
<br />
<br />
<br />
<br />


 - Paste the copied IOCs into the freetext import tool.

<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/pa01aHy.png">
<br />
<br />
<br />
<br />


 - Verify that all IOCs have the correct Category and Type assigned, then click submit.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/y3dKgw9.png">
<br />
<br />
<br />
<br />


 - The MISP workers will now import these IOCs into the event. This process may take a few minutes.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/6opi8vM.png">
<br />
<br />
<br />
<br />


 - Once complete, you'll see all the IOCs successfully imported and stored within MISP.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/sN5NoVl.png">
<br />
<br />
<br />
<br />

---
## Tagging and Finalizing


 - Enhance the event by adding custom tags to better define it.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/zgC1ueH.png">
<br />
<br />
<br />
<br />

 - Experiment with different tags to categorize and describe the event effectively.
<p align="center">
<br/>
<img width="597" alt="Portfolio" src="https://i.imgur.com/HkqQWOk.png">
<br />
<br />
<br />
<br />

 - Return to the Dashboard and observe the Trending Tags widget, which should now display results based on the stored events.
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

