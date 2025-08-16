## Instruction to install in Linux

### Download and Install
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

### Removed already installed VScode
```
# Make sure to remove it if the program was installed from a .deb package
sudo apt remove code

# Remove all configuration related
sudo apt purge code

# Clean up leftover dependencies:
sudo apt autoremove

# Check that is correctly removed
which code
```

### Create a symbolic link to the app
``` 
sudo ln -s ~/programs/vscode/code /usr/local/bin/code
``` 

Now we should be able to start vscode just by executing "code" in the console

