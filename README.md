With curl:

curl -fsSL https://henriquedias.com/filemanager/get.sh | bash

Or using wget:

wget -qO- https://henriquedias.com/filemanager/get.sh | bash

If you’re on Windows, you can use PowerShell to install File Manager too. You should run the following command as administrator since it needs permissions to add the executable to the PATH:

iwr -useb https://henriquedias.com/filemanager/get.ps1 | iex
