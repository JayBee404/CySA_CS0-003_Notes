Data Acquisition - Method and tools used to create a forensically sound copy of data from a source device, such as system memory of a hard disk

BYOD policies complicate data acquisition since you may not be able to legally search or seize the device

Some data can only be collected once the system is shut down or the power gets disconnected

Analysts should always follow the order of volatility when collecting evidence

- CPU registers and cache memory
- Contents of system memory (RAM), routing tables, ARP cache, process table, temporary swap files
- Data on persistent mass storage (HDD/SSD/flash drives)
- Remote logging and monitoring data
- Physical configuration and network topology
- Archival media

--WARNING--
While most of the Windows registry is stored on the disk, some keys (like HKLM\Hardware) are only stored in memory so you should analyze the Registry via memory dump

