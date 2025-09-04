Reverse Engineering - The process of analyzing the structure of hardware or software to reveal more about how it functions

Malware writers often obfuscate the code before it is assembled or compiled to prevent analysis

Disassembler - A computer program that translates machine language into assembly language

Machine Code - The binary code executed by the processor, typically represented as 2 hex digitis for each byte

File Signature (Magic Number) - The first two bytes of a binary header that indicates its file type

When reading the first two bytes of a Windows portable executable file (EXE, DLL, SYS, DRV, or COM), it will always start with `4D5A` in hex, `MZ` in ASCII, or `TV` in Base64 encoding.

Assembly Code - The native processor instructions used to implement the program

Decomplier - Software that translates a binary or low-level machine language code into higher-level code

High-level Code - Real or pseudocode in human readable form that makes it easier to identify functions, variables, and programming logic used in the code

Reverse engineers attempt to identify malware by finding strings to use as a signature for rule-based detection

String - Any sequence of encoded characters that appears within the executable file

Strings tool (native on Linux, part of SysInternals on Windows) will dump all strings with over three characters in ASCII or Unicode encoding

Program Packer - A method of compression in which an executable is mostly compressed and the part that isn't compressed contains the code to decompress the executable

**NOTE** - Just because a program is packed, that doesn't mean it is malicious since many proprietary software also uses packing to deter theft and piracy

Until it is unpacked, packed malware can mask strings and effectively modify its signatures to avoid triggering signature-based scanners

