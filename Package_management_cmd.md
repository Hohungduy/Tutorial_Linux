--------------------------------------------------------------------------
			**Tutorial for package management**
--------------------------------------------------------------------------

1. Installing and Remove solfware in Ubuntu

  (Can use dpkg)
 
  `sudo apt-get update`

  `sudo apt-get install xxxx`
 
  `sudo apt-get remove xxxx`
 
  `sudo apt-get check xxxx`
 
  `sudo apt-get  autoremove xxxx`

2. Getting and Unpack package

  `wget -P /usr/local/src http://ftp.gnu.org/gnu/hello/hello-2.7.tar.Gz`
  
  --     directory to save    path to remote server to pull solfware

  `tar -xvzf hello-2.7.tar.gz`

  -- unpack and decompress the hello archive.
 
  -- z:involves gzip to decompress. v:tells tar to show the name of file

3. Configuring the Package
  
  --Each package will have several features that can be enabled or disabled
   
   `./configure --help`
   
   `./configure` 

4. Compiling the package 

   -- Learning more Makefile

   `make`

   -- Read all Makefile that were created by the configure script. These files tell

    make which files to compile and the order in which to compile them
5.  Installing the Package 
    
    `make install`
6. Remove
    
    `rm -rf xxx`

