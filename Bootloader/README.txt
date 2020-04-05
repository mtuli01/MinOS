*******Requirements******

You need an assember that can convert your assembly instructions to raw binary format and an simulator to view.
I am using Nasm and Qemu simulator.

For Linux, type following commands to install nasm & qemu(Quick Emulator)

	sudo apt-get install nasm
	sudo apt-get install qemu qemu-system-x86_64

	
For Windows,download them from following sites and install them.

	http://www.nasm.us/
	https://qemu.weilnetz.de/



*******To run*******


For Linux,Type following command to compile file
	
		nasm -f bin Welcome.asm -o myos.bin
		
Once file is compiled successfully and myos.bin file is created, then run it in qemu.	

		qemu-system-x86_64 myos.bin
		

For windows, open nasm application, it will prompt a command at location where nasm is installed.
Perform same commands as performed for linux juts giving full file name path.

		nasm.exe -f bin "D:\why\projects\os project\OS-master\Global_Descriptor_Table\asm\gdt.asm" -o "D:\why\projects\os project\OS-master\Global_Descriptor_Table\asm\gdt.bin"
		
		and to run in qemu,
		
		"C:\Program Files\qemu\qemu-system-x86_64.exe"  "D:\why\projects\os project\OS-master\Global_Descriptor_Table\asm\gdt.bin"
		
where i have installed qemu.

Here i have created .bin file, but you can also create .iso file.

Once it successfully prints Hello World! then attach Secondary device/USB drive and boot .bin/.iso in it.
You can use dd command on linux or can use rufus software on windows.
