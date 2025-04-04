# General PowerShell Commands for Windows

---

## **Basic Commands**

1. **`Get-Help`**  
   Displays help information about cmdlets and functions.  
   **Example:** `Get-Help Get-Process`

2. **`Clear-Host`**  
   Clears the console screen.  
   **Example:** `Clear-Host`

3. **`Exit`**  
   Exits the PowerShell session.  
   **Example:** `Exit`

4. **`Echo`**  
   Outputs a string to the console.  
   **Example:** `Echo "Hello, World!"`

5. **`Set-Location`** (Alias: `cd`)  
   Changes the current working directory.  
   **Example:** `Set-Location C:\Users\YourName\Documents`

---

## **File and Directory Management**

6. **`Get-ChildItem`** (Alias: `dir`)  
   Lists files and folders in the current directory.  
   **Example:** `Get-ChildItem`

7. **`Copy-Item`**  
   Copies an item (file or folder) to a specified path.  
   **Example:** `Copy-Item C:\file.txt D:\Backup\`

8. **`Remove-Item`** (Alias: `del`)  
   Deletes a file or folder.  
   **Example:** `Remove-Item C:\file.txt`

9. **`Move-Item`**  
   Moves a file or folder from one location to another.  
   **Example:** `Move-Item C:\file.txt D:\Backup\`

10. **`Rename-Item`**  
    Renames a file or folder.  
    **Example:** `Rename-Item C:\file.txt newfile.txt`

11. **`New-Item`**  
    Creates a new item (file, folder, etc.).  
    **Example:** `New-Item -Path C:\ -Name "newfolder" -ItemType Directory`

## To create a file and write content to it:

```
  "Your content goes here" | Out-File "filename.txt"
```

12. **`Remove-Item`**  
    Removes a file or folder.  
    **Example:** `Remove-Item D:\oldfolder`

---

## **System Information and Diagnostics**

13. **`Get-Process`**  
    Lists all currently running processes.  
    **Example:** `Get-Process`

14. **`Stop-Process`**  
    Stops a process by its name or ID.  
    **Example:** `Stop-Process -Name "chrome"`

15. **`Get-Service`**  
    Lists all services on the system.  
    **Example:** `Get-Service`

16. **`Start-Service`**  
    Starts a stopped service.  
    **Example:** `Start-Service -Name "wuauserv"`

17. **`Get-EventLog`**  
    Retrieves events from the event log.  
    **Example:** `Get-EventLog -LogName Application`

18. **`Get-ComputerInfo`**  
    Displays information about the computer system.  
    **Example:** `Get-ComputerInfo`

19. **`Test-Connection`** (Alias: `ping`)  
    Tests network connectivity to a remote host.  
    **Example:** `Test-Connection google.com`

20. **`Get-WmiObject`**  
    Retrieves management information from local or remote computers.  
    **Example:** `Get-WmiObject -Class Win32_OperatingSystem`

---

## **User Management**

21. **`Get-LocalUser`**  
    Lists all local user accounts on the system.  
    **Example:** `Get-LocalUser`

22. **`New-LocalUser`**  
    Creates a new local user account.  
    **Example:** `New-LocalUser -Name "username" -Password (ConvertTo-SecureString "password" -AsPlainText -Force)`

23. **`Set-LocalUser`**  
    Modifies a local user account.  
    **Example:** `Set-LocalUser -Name "username" -PasswordNeverExpires $True`

24. **`Remove-LocalUser`**  
    Deletes a local user account.  
    **Example:** `Remove-LocalUser -Name "username"`

---

## **Disk and File System Operations**

25. **`Get-Disk`**  
    Lists all physical disks.  
    **Example:** `Get-Disk`

26. **`New-Partition`**  
    Creates a new partition on a disk.  
    **Example:** `New-Partition -DiskNumber 1 -UseMaximumSize -AssignDriveLetter`

27. **`Format-Volume`**  
    Formats a volume.  
    **Example:** `Format-Volume -DriveLetter D -FileSystem NTFS -Confirm:$false`

28. **`Get-Volume`**  
    Retrieves the volume information for drives.  
    **Example:** `Get-Volume`

29. **`Optimize-Volume`**  
    Defragments or optimizes a volume.  
    **Example:** `Optimize-Volume -DriveLetter C -ReTrim -Verbose`

---

## **Network Configuration and Utilities**

30. **`Get-NetIPAddress`**  
    Displays IP address configuration information.  
    **Example:** `Get-NetIPAddress`

31. **`Test-NetConnection`** (Alias: `tracert`)  
    Tests network connection to a remote host.  
    **Example:** `Test-NetConnection google.com`

32. **`Get-NetAdapter`**  
    Retrieves network adapter information.  
    **Example:** `Get-NetAdapter`

33. **`Set-NetIPAddress`**  
    Configures an IP address on a network adapter.  
    **Example:** `Set-NetIPAddress -InterfaceAlias "Ethernet" -IPAddress 192.168.1.100 -PrefixLength 24 -DefaultGateway 192.168.1.1`

---

## **PowerShell Scripting and Automation**

34. **`Get-Command`**  
    Lists all cmdlets, functions, workflows, and aliases in the session.  
    **Example:** `Get-Command`

35. **`Get-Content`**  
    Retrieves the content of a file.  
    **Example:** `Get-Content C:\file.txt`

36. **`Set-Content`**  
    Writes content to a file.  
    **Example:** `Set-Content C:\file.txt "Hello, PowerShell!"`

37. **`Out-File`**  
    Sends output to a file.  
    **Example:** `Get-Process | Out-File C:\processes.txt`

38. **`ForEach-Object`**  
    Performs an operation for each object in a pipeline.  
    **Example:** `Get-Process | ForEach-Object { $_.Name }`

39. **`If`**  
    Executes a block of code conditionally.  
    **Example:**
    ```powershell
    if ($value -eq 10) {
        Write-Host "Value is 10"
    }
    ```

---

### How to Save:

1. Copy the above content.
2. Open **VSCode** and create a new file.
3. Paste the content into the file.
4. **Save** the file as `PowerShell_Commands.md` or any name you'd prefer.

---
