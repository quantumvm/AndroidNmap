AndroidNmap
===========

Working MakeFile for Android 6.47

The make file is based on the one found here: https://github.com/kost/nmap-android/blob/master/android/Makefile but it wasnt working.

USE:
1. Copy android folder into the nmap-6.47 directory.
2. Run make doit
3. Profit

Caveats:
If you are compiling from bash you will have to modify the android NDK. At line 723 you need to change:

for ABI in $(tr ',' ' ' <<< $ABIS); do
to
for ABI in $(echo "$ABIS" | tr ',' ' '); do
