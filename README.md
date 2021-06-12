# windows-terminal-config
my personal windows terminal config file

copy-paste content from `settings.json` to Windows Terminal profile

------

## Powershell Configuration  

Detailed information can be found here:
[Setup Tutorial](https://docs.microsoft.com/en-us/windows/terminal/tutorials/powerline-setup)  

Steps:  
1. Go [Nerd Fonts Website](https://www.nerdfonts.com/font-downloads) and download `Mononoki Nerd Font`, and install them system wise  
2. Copy `.oh-my-posh.omp.json` and put it under home (`~`) directory  
3. Run Commands
   ```powershell
   Install-Module posh-git -Scope CurrentUser  
   Install-Module oh-my-posh -Scope CurrentUser
   notepad $PROFILE
   ```  
   Or if you have [vscode](https://code.visualstudio.com/) installed, the last command can be:
   ```powershell
   code $PROFILE
   ```
4. In notepad(or vscode), add the following lines  
   ```powershell
   Import-Module posh-git
   Import-Module oh-my-posh
   Set-PoshPrompt -Theme ~/.oh-my-posh.omp.json
   
   Set-PSReadLineOption -Colors @{Operator="Gray"}
   Set-PSReadLineOption -Colors @{Parameter="Magenta"}
   ```

May also need to modify powershell execution policy:  
```powershell
Set-ExecutionPolicy RemoteSigned
```

Can also set vscode font to `mononoki NF`, so that the inside terminal can correctly display the characters  

------

## Demo  

![img](demo.png)
