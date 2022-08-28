unowfs
======

Port of the utility to extract files from OWFS file system images wrote by Craig Heffner.


可以用来提取tplink路由器中的文件
环境python3.x


binwalk
DECIMAL       HEX           DESCRIPTION
-------------------------------------------------------------------------------------------------------
14702         0x396E        Linux Journalled Flash filesystem, little endian
14868         0x3A14        LZMA compressed data, properties: 0x6E, dictionary size: 8388608 bytes, uncompressed size: 2415648 bytes
733540        0xB3164       Wind River management filesystem, compressed, 138 files
733542        0xB3166       Wind River management filesystem, 9043969 files
743520        0xB5860       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 716 bytes
743888        0xB59D0       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 834 bytes
744352        0xB5BA0       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 740 bytes
744772        0xB5D44       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 1284 bytes
745380        0xB5FA4       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 1600 bytes
746136        0xB6298       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 1596 bytes
746900        0xB6594       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 855 bytes
747396        0xB6784       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 2780 bytes
748488        0xB6BC8       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 1424 bytes
749220        0xB6EA4       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 685 bytes
749652        0xB7054       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 1142 bytes
750132        0xB7234       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 1827 bytes
750916        0xB7544       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 4638 bytes
752280        0xB7A98       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 1700 bytes
…………………………


There is a filesystem!

733540        0xB3164       Wind River management filesystem, compressed, 138 files


Let's extract it: (0xB3164 = 733540 in decimal)

dd if=wr541gv7_en_4_7_13_up.bin bs=733540 skip=1 of=fs.bin

python unowfs.py fs.bin      

Now enter the "extracted" folder. This are the contents:

AdvScrRpm.htm
AssignedIpAddrListHelpRpm.htm
AssignedIpAddrListRpm.htm
AuthError.htm
BackNRestoreHelpRpm.htm
BakNRestoreRpm.htm 
………………………………
