# Installing-Linux-Ubuntu-Steps
How to install Linux Ubuntu on a PC 

<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=<device-width>, initial-scale=1.0">
        <title>Installing a Linux server on a {C</title>
        <style>
            body {
                font-family: Arial, sans-serif;
                line-height: 1.6;
                padding: 20px;
            }
            h2 {
                margin-top: 40px;
            }
            ol {
            margin-bottom: 20px;
            }
            li {
                margin-bottom: 10px;
            }
            a {
                color: blue;
                text-decoration: underline;
            }
        </style>
    </head>
<body>
    <h1>Create Bootable USB with Ubuntu Server</h1>

    <!-- Step 1: Download Ubuntu Server ISO -->
    <h2>Step 1: Download Ubuntu Server ISO</h2>
    <ol>
        <li>Go to the official Ubuntu website: <a href="https://ubuntu.com/download/server">https://ubuntu.com/download/server</a></li>
        <li>Download the Ubuntu Server ISO file. Choose the appropriate version.</li>
    </ol>

    <!-- Step 2: Prepare the USB Drive -->
    <h2>Step 2: Prepare the USB Drive</h2>
    <ol>
        <li>Insert your USB drive into your computer.</li>
        <li>Make sure the USB drive is empty, as the following steps will erase all data on it.</li>
    </ol>

    <!-- Step 3: Create a Bootable USB Drive with balenaEtcher -->
    <h2>Step 3: Create a Bootable USB Drive with balenaEtcher</h2>
    <ol>
        <li>Download and install balenaEtcher from the official website: <a href="https://www.balena.io/etcher/">https://www.balena.io/etcher/</a></li>
        <li>Open balenaEtcher.</li>
        <li>Click on the "Flash from file" button and select the Ubuntu Server ISO file.</li>
        <li>Select your USB drive.</li>
        <li>Click on the "Flash!" button to create the bootable USB drive.</li>
        <li>Once the process is complete, eject the USB drive.</li>
    </ol>

    <!-- Step 4: Boot from the USB Drive -->
    <h2>Step 4: Boot from the USB Drive</h2>
    <ol>
        <li>Insert the bootable USB drive into the machine where you want to install Ubuntu Server.</li>
        <li>Start or restart the machine.</li>
        <li>During startup, access the BIOS or UEFI settings. The key to access these settings varies depending on the manufacturer (e.g. F2, F10, F12, or Del).</li>
        <li>In the BIOS or UEFI settings, change the boot sequence to prioritize booting from the USB drive.</li>
        <li>Save the changes and exit the BIOS or UEFI settings.</li>
    </ol>

    <!-- Step 5: Install Ubuntu Server -->
    <h2>Step 5: Install Ubuntu Server</h2>
    <ol>
        <li>The machine should now boot from the USB drive and load the Ubuntu Server installer.</li>
        <li> clic try or install you ubuntu server.</li>
        
    </ol>

    <!-- Step 6: Complete Installation -->
    <h2>Step 6: Complete Installation</h2>
    <ol>
        <li>Once the installation process is complete, remove the USB drive from the machine.</li>
        <li>Restart the machine.</li>
        <li>Ubuntu Server should now be installed.</li>
    </ol>


    <h1>Steps to install WSL on Windows</h1>
    *So that you can ssh into the remote linux server, (although you could just ssh from powershell or cmd), but using ubunutu just simplifies the enrivonment
    <ol>
        <li>Open cmd.exe with administrator.</li>
        <li>Type <code>wsl --install</code>.</li>
        <li>The following is a list of valid distributions that can be installed. Install using <code>wsl --install -d &lt;Distro&gt;</code>.</li>

    <table>
        <caption>Operating Systems</caption>
        <thead>
            <tr>
                <th>NAME</th>
                <th>FRIENDLY NAME</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>Ubuntu</td>
                <td>Ubuntu</td>
            </tr>
            <tr>
                <td>Debian</td>
                <td>Debian GNU/Linux</td>
            </tr>
            <tr>
                <td>kali-linux</td>
                <td>Kali Linux Rolling</td>
            </tr>
            <tr>
                <td>Ubuntu-18.04</td>
                <td>Ubuntu 18.04 LTS</td>
            </tr>
            <tr>
                <td>Ubuntu-20.04</td>
                <td>Ubuntu 20.04 LTS</td>
            </tr>
            <tr>
                <td>Ubuntu-22.04</td>
                <td>Ubuntu 22.04 LTS</td>
            </tr>
            <tr>
                <td>OracleLinux_7_9</td>
                <td>Oracle Linux 7.9</td>
            </tr>
            <tr>
                <td>OracleLinux_8_7</td>
                <td>Oracle Linux 8.7</td>
            </tr>
            <tr>
                <td>OracleLinux_9_1</td>
                <td>Oracle Linux 9.1</td>
            </tr>
            <tr>
                <td>openSUSE-Leap-15.5</td>
                <td>openSUSE Leap 15.5</td>
            </tr>
            <tr>
                <td>SUSE-Linux-Enterprise-Server-15-SP4</td>
                <td>SUSE Linux Enterprise Server 15 SP4</td>
            </tr>
            <tr>
                <td>SUSE-Linux-Enterprise-15-SP5</td>
                <td>SUSE Linux Enterprise 15 SP5</td>
            </tr>
            <tr>
                <td>openSUSE-Tumbleweed</td>
                <td>openSUSE Tumbleweed</td>
            </tr>
        </tbody>
    </table>
        <li>I chose Ubuntu 22.04: <code>wsl --install -d Ubuntu-22.04</code>.</li>
        <li>Encountered error:
            <ul>
                <li>Installing, this may take a few minutes...</li>
                <li>WSLRegisterDistribution failed with error: 0x800701bc</li>
                <li>Error: 0x800701bc WSL 2 requires an update to its kernel component. For information please visit <a href="https://aka.ms/wsl2kernel">https://aka.ms/wsl2kernel</a></li>
                <li>Download the latest package:
                    <ul>
                        <li><a href="#">WSL2 Linux kernel update package for x64 machines</a></li>
                    </ul>
                </li>
                <li>Downloaded, follow instructions on the wizard.</li>
            </ul>
        </li>
        <li>Set WSL 2 as a default version: <code>wsl --set-default-version 2</code>.</li>
        <li>Encountered error:
            <ul>
                <li><code>wsl --set-default-version 2</code></li>
                <li>Please enable the Virtual Machine Platform Windows feature and ensure virtualization is enabled in the BIOS.</li>
                <li>For information please visit <a href="https://aka.ms/enablevirtualization">https://aka.ms/enablevirtualization</a>.</li>
                <li>Press start, type "windows features" - select enable virtualization.</li>
                <li>Restart terminal.</li>
            </ul>
        </li>
        <li>Open terminal, select "Ubuntu 22.04":
            <ul>
                <li>Installing, this may take a few minutes...</li>
                <li>Please create a default UNIX user account. The username does not need to match your Windows username.</li>
                <li>For more information visit: <a href="https://aka.ms/wslusers">https://aka.ms/wslusers</a></li>
                <li>Enter new UNIX username: andrehasoon</li>
                <li>New password:</li>
                <li>Retype new password:</li>
                <li>Passwd: password updated successfully.</li>
                <li>Installation successful! Windows Subsystem for Linux is now available in the Microsoft Store!</li>
                <li>You can upgrade by running <code>wsl.exe --update</code> or by visiting <a href="https://aka.ms/wslstorepage">https://aka.ms/wslstorepage</a>.</li>
                <li>Installing WSL from the Microsoft Store will give you the latest WSL updates, faster.</li>
                <li>For more information please visit <a href="https://aka.ms/wslstoreinfo">https://aka.ms/wslstoreinfo</a>.</li>
            </ul>
        </li>
        <li>Run <code>wsl.exe --update</code>.</li>
    </ol>

    <h1>Steps to add a sudo user on Linux server</h1>
    <ol>
        <li>SSH onto the server. <code>ssh [username]@ip</code></li>
        <li>Type <code>sudo adduser [username]</code>.</li>
        <li>Type <code>sudo usermod -aG sudo [username]</code>.</li>
        <li>Check to see if the new user has sudo privileges: <code>groups [username]</code>.</li>
    </ol>
    
   <!-- How to creat a configuration file for ssh -->
   <h1>How to create a configuration file for SSH</h1>
   <ol>
       <li><strong>Navigate to SSH Configuration Directory:</strong>
           <ul>
               <li>Open a terminal or command prompt.</li>
               <li>Navigate to the SSH configuration directory.</li>
               <li>Linux/ubuntu <code>cd ~/.ssh/</code></li>

           </ul>
       </li>
       <li><strong>Create or Edit the SSH Configuration File:</strong>
           <ul>
               <li>If the <code>config</code> file already exists, open it in a text editor. If not, create a new file named <code>touch config</code>.</li>
               <li>Add configurations for each host you want to connect to.</li>
           </ul>
       </li>
       <li><strong>Add Host Configuration:</strong>
           <ul>
               <li>In the <code>config</code> file, add configurations for each host you want to connect to.</li>
               <li>Each host configuration should be formatted as follows:</li>
               <li><code>Host alias<br></b>&emsp;HostName IP_address_or_hostname<br>&emsp;User username</code></li>
               <li>Replace <code>alias</code> with a shorthand name for the host, <code>IP_address_or_hostname</code> with the IP address or hostname of the remote server, and <code>username</code> with your username on the remote server.</li>
           </ul>
       </li>
       </ol>
       
<!-- How to add puiblic/private keys on ssh to enable passwordless login -->
       <h1>How to add public/private keys on SSH to enable passwordless login</h1>
       <h2>Open WSL Terminal:</h2>
       <ul>
           <li>
               <p>Open the WSL terminal on your Windows 11 machine.</p>
           </li>
       </ul>
       
       <h2>Generate SSH Key Pair:</h2>
       <ul>
           <li>
               <p>Use the <code>ssh-keygen</code> command to generate a new SSH key pair.</p>
           </li>

           <li>
               <p>Press Enter to accept the default file location (<code>~/.ssh/id_rsa</code>).</p>
           </li>
       </ul>
       
       <h2>Confirm Key Generation:</h2>
       <ul>
           <li>
               <p>After running the <code>ssh-keygen</code> command, you'll see output indicating that the key pair has been generated. It will display the location of the public and private keys, the key fingerprint and the keys random art image.</p>
        </li>
       </ul>
       
       <h2>Copy Public Key to Server:</h2>
       <ul>
           <li>
               <p>Use the <code>ssh-copy-id</code> command to copy your public key to the server.</p>
           </li>
           <li>
               <pre><code>ssh-copy-id username@server_ip</code></pre>
           </li>
           <li>
               <p>You'll be prompted to enter your password for the server. Once authenticated, your public key will be added to the <code>~/.ssh/authorized_keys</code> file on the server.</p>
           </li>
       </ul>
       
       <h2>Test SSH Connection:</h2>
       <ul>
           <li>
               <p>Once your public key is added to the server's <code>authorized_keys</code> file, you should be able to SSH into the server without entering a password.</p>
           </li>
           <li>
               <pre><code>ssh username@server_ip</code></pre>
           </li>
           <li>
               <p>If everything is set up correctly, you should be logged into the server without being prompted for a password.</p>
           </li>
       </ul>
       
       <h2>Optional: Protect Private Key (Windows Side):</h2>
       <ul>
           <li>
               <p>On the Windows side, you can protect your private key by setting appropriate permissions on the <code>.ssh</code> directory and the private key file (<code>id_rsa</code>).</p>
           </li>
       </ul>
       
       
 

</body>
</html>