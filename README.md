```
unowfs
```

2

```
======
```

3

```

```

4

```
Port of the utility to extract files from OWFS file system images wrote by Craig Heffner.
```

5

```

```

6

```

```

7

```
可以用来提取tplink路由器中的文件
```

8

```
环境python3.x
```

9

```

```

10

```

```

11

```
binwalk
```

12

```
DECIMAL       HEX           DESCRIPTION
```

13

```
-------------------------------------------------------------------------------------------------------
```

14

```
14702         0x396E        Linux Journalled Flash filesystem, little endian
```

15

```
14868         0x3A14        LZMA compressed data, properties: 0x6E, dictionary size: 8388608 bytes, uncompressed size: 2415648 bytes
```

16

```
733540        0xB3164       Wind River management filesystem, compressed, 138 files
```

17

```
733542        0xB3166       Wind River management filesystem, 9043969 files
```

18

```
743520        0xB5860       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 716 bytes
```

19

```
743888        0xB59D0       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 834 bytes
```

20

```
744352        0xB5BA0       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 740 bytes
```

21

```
744772        0xB5D44       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 1284 bytes
```

22

```
745380        0xB5FA4       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 1600 bytes
```

23

```
746136        0xB6298       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 1596 bytes
```

24

```
746900        0xB6594       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 855 bytes
```

25

```
747396        0xB6784       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 2780 bytes
```

26

```
748488        0xB6BC8       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 1424 bytes
```

27

```
749220        0xB6EA4       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 685 bytes
```

28

```
749652        0xB7054       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 1142 bytes
```

29

```
750132        0xB7234       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 1827 bytes
```

30

```
750916        0xB7544       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 4638 bytes
```

31

```
752280        0xB7A98       LZMA compressed data, properties: 0x5A, dictionary size: 8388608 bytes, uncompressed size: 1700 bytes
```

32

```
…………………………
```

33

```

```

34

```

```

35

```
There is a filesystem!
```

36

```

```

37

```
733540        0xB3164       Wind River management filesystem, compressed, 138 files
```

38

```

```

39

```

```

40

```
Let's extract it: (0xB3164 = 733540 in decimal)
```

41

```

```

42

```
dd if=wr541gv7_en_4_7_13_up.bin bs=733540 skip=1 of=fs.bin
```

43

```

```

44

```
python unowfs.py fs.bin      
```

45

```

```

46

```
Now enter the "extracted" folder. This are the contents:
```

47

```

```

48

```
AdvScrRpm.htm
```

49

```
AssignedIpAddrListHelpRpm.htm
```

50

```
AssignedIpAddrListRpm.htm
```

51

```
AuthError.htm
```

52

```
BackNRestoreHelpRpm.htm
```

53

```
BakNRestoreRpm.htm 
```

54

```
………………………………
```

55
