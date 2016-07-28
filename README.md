
This repo includes the necessary libs for EPOS....

EPOS Command Library

1) Download and extract the zip file to a temporary directory.

2) Select your target architecture directory (x86, x86_64, arm hf/sf/rpi).

   a) x86: 32-bit operating system for Intel/AMD processors

   b) x86_64: 64-bit operating system for Intel/AMD processors

   c) arm rpi: 32-bit operating system (hard float) for ARMv6 processors

   d) arm sf/hf: 32-bit operating system (soft/hard float) for ARMv7 processors

3) Take note that the following actions will require root privileges.

4) Copy the shared library file “libEposCmd.so.5.0.1.0” to the directory “/usr/local/lib”:

   a) sudo cp libEposCmd.so.5.0.1.0 /usr/local/lib

   b) Create a soft link to this library into directory “/usr/local/lib”.Execute the following commands:

      $ cd /usr/local/lib
      
      $ sudo ln -s libEposCmd.so.5.0.1.0 libEposCmd.so
   
   c) Create a soft link to this library into directory “/usr/lib” (or any directory listed in the LD_LI-BRARY_PATH system variable). Execute the following commands from directory “/usr/lib”:
   
      $ cd /usr/lib
   
      $ sudo ln -s /usr/local/lib/libEposCmd.so libEposCmd.so
   
   d) Alternatively, if you do not plan to use Linux versioning/symlinks system, this single command does the job, too:
     
      $ sudo cp libEposCmd.so.5.0.1.0 /usr/lib/libEposCmd.so

5) Optional: Copy the file “Defintions.h” to the directory “/usr/include”.


