---
title: "GUI"
weight: 10
description: "graphical user interface (Windows / Linux / OS X / Unix)"
---

### MobaXterm (Win)

If you are on Windows, you can directly use [MobaXterm](https://mobaxterm.mobatek.net/) to transfer files.

Connect to your session. On the left panel you should see an **SFTP** panel opened.

- You have just to drag and drop your files to this panel to **transfer** files to the cluster.

- To retrieve a file from the cluster, you can right click on it and choose the **Download** option.

Please refers to [MobaXterm documentation](https://mobaxterm.mobatek.net/documentation.html) for more informations on the available features.

### FileZilla (Windows / Linux / OS X / Unix)

- Download the FileZilla client application from [filezilla-project.org](https://filezilla-project.org/download.php?type=client) and install it.

- First we need to add our session:
  - Start the application.

  - click on the **Site Manager** button on the top left or select **Site Manager** from the **File** menu.

  - Click on the **New Site** button and enter/select the following:

    ```
    - Host: <IP_address>
    - Port: 22
    - Protocol: SFTP - SSH File Transfer Protocol
    - Logon Type: Normal
    - User: <username>
    - Password : <passward>
    ```

  - Click on the `Connect` button.

- On the very top, beneath the quick connect, you see the **message log**. Below you have the directory tree and the contents of the current directory for you local computer on the left and the remote location on the right.

- To **transfer a file**, simply drag and drop it from the directory listing on the left side to destination directory on the right (to transfer from local to remote) or vice versa (to transfer from remote to local). You can also select a file by left clicking on it once and then right click on it to get the context menu and select "Upload" or "Download" to transfer it.

- When you click the fifth icon on the top with the two green arrows to toggle the transfer queue, you can see **the status of ongoing transfers** on the very bottom of the window.

{{% notice note %}}

If you can't connect to the cluster with this error: `Error:	Server unexpectedly closed network connection Error:	Could not connect to server` <br><br/>Please **allow FileZilla in Firewall**. Go to Windows Defender Firewall --> Allowed Apps--> Allow another app and then add FileZilla (**filezilla.exe and fzsftp.exe**) from where you install it.

{{% /notice %}}

