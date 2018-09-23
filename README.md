# Linux-File-System
Linux File System Step by Step

EXT3 File System
----------------

Individual file size 16 GB to 2 TB

Overall ext3 file system size 2TB to 32 TB

Directory can contain a maximum of 32,000 subdirectories

The main benefit of ext3 is that it allows journaling.

Journal – Metadata and content are saved in the journal.

You can convert a ext2 file system to ext3 file system directly (without backup/restore).

Ext2 to Ext3 Convertion
-----------------------

umount /dev/sda2

tune2fs -j /dev/sda2

mount /dev/sda2 /home


Ext4 File System
----------------

Individual file size can be from 16 GB to 16 TB

Overall maximum ext4 file system size is 1 EB (exabyte)

Directory can contain a maximum of 64,000 subdirectories.

You can also mount an existing ext3 fs as ext4 fs (without having to upgrade it).

It has journal checksum. fast fsck, etc.

Ext3 to Ext4 Convertion
-----------------------

umount /dev/sda2

tune2fs -O extents,uninit_bg,dir_index /dev/sda2

e2fsck -pf /dev/sda2

mount /dev/sda2 /home


XFS File System
---------------

Maximum File Size - 500 TB

Overall maximum ext4 file system size is 500 TB

Advantages
----------

Encryption

Compression

Snapshot

Deduplication


Fat 32 File System
------------------

Maximum File Size 4 GB

Maximum Volume Size 2 TB

Maximum File Name - 8.5 Char

NTFS File Size
--------------

Maximum File Size - 16 TB

Maximum Volume Size - 256 TB

Compression - yes

Fault Tolerance - Auto Repair
