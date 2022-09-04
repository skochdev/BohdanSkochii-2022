# Building nvim from source and setup configs

Remove nvim

`sudo rm /usr/local/bin/nvim`

Clone this to your home or any other dir

`git clone git@github.com:neovim/neovim.git`

`git checkout release-0.7` or any other release you want

`make CMAKE_BUILD_TYPE=Release`
`sudo make install`

install `tree` for terminal

`sudo apt install tree`

![[Pasted image 20220903192544.png]]