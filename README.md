# Alacritty-Config
Just my personal alacritty config, I use it as my main, I also use py-wal. There will be instructions on how to use that.
Make sure to use the alacritty terminal, other terminals won't work

## How to install Alacritty:

Arch Linux: `sudo pacman -S alacritty`
 
Debian/Ubuntu Based: `sudo apt install alacritty`
  
Fedora: `sudo dnf install alacritty` 

Steps to use my config :
#### 1. make a directory (if not already made) by running: 
```bash                        
mkdir ~/.config/alacritty/
```

#### 2. Copy my config into the newly created directory by runnning the following commands: 
                
```bash                                            
cd ~/.config/alacritty

git clone https://github.com/atreyaved/Alacritty-Config.git

cd Alacritty-config

mv alacritty.yml ~/.config/alacritty
```
#### 3. Now just restart alacritty

Steps to install py-wal:
> _Pywal is basically changed your terminal color scheme according to a image_

## 1. Install the package:

- Arch Linux:
```bash
sudo pacman -S python-pywal
```
- Debian/Ubuntu based distros:
```bash
sudo apt insatll sudo apt install python3-pip
sudo pip3 install pywal    
```
- Fedora: 
```bash
sudo dnf install python3-pip
sudo pip3 intsall pywal
```
## 2. Use pywal: 
`wal -i <path_to_your_image>` for the image I recommend just using your wallpaper

## 3. Starting automatically: 
Now that you have installed pywal, we are gonna start it whenever your terminal starts, to do that, do the following
`nano ~/.bashrc` (or your favorite text editor)

Now paste the following lines to the end of the file:
```bash
# Import colorscheme from 'wal' asynchronously
# &   # Run the process in the background.
# ( ) # Hide shell job control messages.
(cat ~/.cache/wal/sequences &)
# Alternative (blocks terminal for 0-3ms)
cat ~/.cache/wal/sequences
# To add support for TTYs this line can be optionally added.
source ~/.cache/wal/colors-tty.sh
```
And boom! now you have a beautiful terminal.
