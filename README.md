# Instruction to install in Linux

1. Download the .tar from the webpage 
2. Create a folder wherever you want it: vscode
3. Untar the folder into this directory:
```
# We need to create the vscode folder before
mkdir vscode

# Untar the downloaded vscode
tar -xvzf code-stable-x64-1755017190.tar.gz -C vscode

# To work correctly it needs the oS Code (Electron) needs the 
# chrome-sandbox helper to have the correct ownership and 
# permissions to run safely. 
sudo chown root:root chrome-sandbox
sudo chmod 4755 chrome-sandbox

# Now we can start code
./code
```

