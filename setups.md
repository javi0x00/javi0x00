# :memo: Notes
## SETUPS

### .vimrc
set encoding=utf-8  
set number  
syntax enable  
colorscheme ron  
filetype on  
augroup C_Python_Settings  
&nbsp;autocmd fileType c source ~/vi-settings/c.vi  
&nbsp;autocmd fileType python source ~/vi-settings/python.vi  
augroup END

### c.vi
set cindent

### python.vi
set tabstop =4  
set softtabstop =4  
set shiftwidth =4  
set expandtab

### Betty linter
* Clone the [Betty repo](https://github.com/holbertonschool/Betty)
* ```cd``` into the Betty directory
* Install the linter with ```sudo ./install.sh```
* New file called ```betty```, and copy the script below:
```
#!/bin/bash
# Simply a wrapper script to keep you from having to use betty-style
# and betty-doc separately on every item.
# Originally by Tim Britton (@wintermanc3r), multiargument added by
# Larry Madeo (@hillmonkey)

BIN_PATH="/usr/local/bin"
BETTY_STYLE="betty-style"
BETTY_DOC="betty-doc"

if [ "$#" = "0" ]; then
    echo "No arguments passed."
    exit 1
fi

for argument in "$@" ; do
    echo -e "\n========== $argument =========="
    ${BIN_PATH}/${BETTY_STYLE} "$argument"
    ${BIN_PATH}/${BETTY_DOC} "$argument"
done
```
* Once saved, exit file and change permissions to apply to all users with ```chmod a+x betty```
* Move the ```betty``` file into ```/bin/``` directory or somewhere else in your ```$PATH``` with ```sudo mv betty /bin/```
* You can now type ```betty <filename>``` to run the Betty linter!

##### :globe_with_meridians: Social
[WebSite](https://www.javierandresgp.com)  |  [GitHub](https://github.com/javierandresgp/)  |  [Linkedin](https://www.linkedin.com/in/javierandresgp/)  |  [Twitter](https://twitter.com/javierandresgp0)  |  [freeCodeCamp](https://www.freecodecamp.org/javierandresgp)  |  [HackerRank](https://www.hackerrank.com/javierandresgp)  |  [StackOverflow](https://stackoverflow.com/users/13728583/javierandresgp)  |  [Medium](https://medium.com/@javierandresgp)  |  [Quora](https://es.quora.com/profile/Javier-Andr%C3%A9s-9)  |  [Meetup](https://www.meetup.com/es/members/305321275/)  |  [Facebook](https://www.facebook.com/javierandresgp0/)  |  [Instagram](https://www.instagram.com/javierandresgp/)

## Software engineer
[Javier Andrés Garzón Patarroyo](https://www.javierandresgp.com)
