# TapasFlashTool

27.07.2021 Python3 FIX "junk" characters. 
```
usage: python -m TapasFlashTool [-h] [-b B] -p port -k kernel_file -a app_file -d 
                                             {f2802x,f2803x,f2805x,f2806x,f2837xD,f2837xS,f2807x}
                                             [-b2 second_baud] [-debug]    
-h for help
```

The first baudrate is set for transferring the flash kernel, the second baudrate will be used for transferring the application file. 


## Creating the hex tables
Texas Instruments provides a tool named hex2000. It is shipped with Code Composer Studio.
Run the hex2000 programm the following:
```
hex2000 binary_file.out -boot -sci8 -a
```

Do this for your application and the flash_kernel then pass the files to the TapasFlashTool.


Tested on a Raspberry Pi and W10.

# References:
https://github.com/SDI-SoftwareDefinedInverter/TAPAS