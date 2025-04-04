# General CMD Commands for Windows

---

## **Basic Commands**

1. **`dir`**  
   Displays a list of files and folders in the current directory.  
   **Example:** `dir`

2. **`cd`** (Change Directory)  
   Changes the current directory.  
   **Example:** `cd C:\Users\YourName\Documents`

3. **`cls`**  
   Clears the command prompt screen.  
   **Example:** `cls`

4. **`echo`**  
   Displays a message or turns on/off command echoing.  
   **Example:** `echo Hello, World!`

   **For CMD**:
   Open the terminal in **CMD** mode and run:

   ```cmd
   echo. > newfile.txt
   ```

   This will create an empty `newfile.txt` file in your current directory.

   ## **Example for creating with name**

   ```
   echo "This is a new file" > filename.txt
   ```

```
     Example for Overwriting a File:
    To overwrite example.txt with new content:

---------------------
    echo Hello, this is new content > example.txt
    ---------------------
```

```
Create/Overwrite a file:

---------------
echo Your content here > filename.txt
Append content to a file:
-------------------

--------------------
echo Your appended content here >> filename.txt
Manual entry with copy con:
---------------------

--------------------
copy con filename.txt
Open a file in Notepad:
-------------------------

notepad filename.txt
```

5. **`exit`**  
   Closes the command prompt window.  
   **Example:** `exit`

---

## **File and Directory Management**

6. **`copy`**  
   Copies one or more files from one location to another.  
   **Example:** `copy file1.txt D:\Backup\`

7. **`del`**  
   Deletes one or more files.  
   **Example:** `del file1.txt`

8. **`move`**  
   Moves files from one location to another.  
   **Example:** `move file1.txt D:\Backup\`

9. **`rename`**  
   Renames a file or directory.  
   **Example:** `rename oldname.txt newname.txt`

10. **`md`** (Make Directory)  
    Creates a new directory.  
    **Example:** `md newfolder`

11. **`rd`** (Remove Directory)  
    Removes an empty directory.  
    **Example:** `rd oldfolder`

---

## **System Information and Diagnostics**

12. **`systeminfo`**  
    Displays detailed configuration information about the computer and its operating system.  
    **Example:** `systeminfo`

13. **`ipconfig`**  
    Displays IP configuration information for all network interfaces.  
    **Example:** `ipconfig /all`

14. **`ping`**  
    Sends a test message to another computer on the network or the internet to check connectivity.  
    **Example:** `ping google.com`

15. **`tasklist`**  
    Lists all currently running processes.  
    **Example:** `tasklist`

16. **`taskkill`**  
    Ends a process by its process ID or image name.  
    **Example:** `taskkill /IM chrome.exe`

17. **`chkdsk`**  
    Checks the disk for errors and can fix issues.  
    **Example:** `chkdsk C: /f`

18. **`sfc /scannow`**  
    Scans and repairs system files.  
    **Example:** `sfc /scannow`

19. **`shutdown`**  
    Shuts down or restarts the computer.  
    **Example:** `shutdown /r /t 30` (Reboot after 30 seconds)

---

## **Network Configuration and Utilities**

20. **`netstat`**  
    Displays active network connections and their statuses.  
    **Example:** `netstat -a`

21. **`tracert`**  
    Traces the route packets take to reach a network host.  
    **Example:** `tracert google.com`

22. **`netsh`**  
    Command-line scripting for network configuration tasks.  
    **Example:** `netsh wlan show profiles`

23. **`nslookup`**  
    Queries DNS to obtain domain name or IP address mapping.  
    **Example:** `nslookup google.com`

---

## **User Management**

24. **`net user`**  
    Displays, adds, or modifies user accounts on the computer.  
    **Example:** `net user username password /add`

25. **`net localgroup`**  
    Displays, adds, or modifies local group memberships.  
    **Example:** `net localgroup administrators username /add`

---

## **Disk Operations**

26. **`diskpart`**  
    Opens a disk partitioning tool for managing disks, partitions, and volumes.  
    **Example:** `diskpart`

27. **`format`**  
    Formats a disk or drive.  
    **Example:** `format D:`

28. **`defrag`**  
    Defragments a drive to optimize file system performance.  
    **Example:** `defrag C:`

---

## **Environment and Configuration**

29. **`set`**  
    Displays, sets, or removes environment variables.  
    **Example:** `set PATH`

30. **`path`**  
    Displays or sets the search path for executable files.  
    **Example:** `path`

31. **`assoc`**  
    Displays or modifies file extension associations.  
    **Example:** `assoc .txt=txtfile`

32. **`regedit`**  
    Opens the Windows Registry Editor.  
    **Example:** `regedit`

---

## **File Compression and Archive**

33. **`compact`**  
    Displays or alters the compression of files or directories.  
    **Example:** `compact /u file.txt` (uncompress)

34. **`tar`**  
    Compresses or extracts tar archives.  
    **Example:** `tar -xvf archive.tar`

35. **`expand`**  
    Expands compressed files.  
    **Example:** `expand file.cab`

---

## **PowerShell (Advanced Tasks)**

36. **`powershell`**  
    Opens the PowerShell command-line interface for more advanced scripting.  
    **Example:** `powershell`

37. **`get-help`**  
    Displays information about PowerShell commands.  
    **Example:** `get-help Get-Process`

---

### How to Save:

1. Copy the above content.
2. Open **VSCode** and create a new file.
3. Paste the content into the file.
4. Save the file as `CMD_Commands.md` or any name you'd prefer.

---
