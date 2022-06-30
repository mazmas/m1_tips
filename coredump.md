# Enable core dump file on an M1/M2 mac

1. On your M1 mac, open a Terminal window.
2. In shell,
>    `% ulimit -c unlimited`
3. Prepare to sign by adding dummy entitlements
>    `% /usr/libexec/PlistBuddy -c "Add :com.apple.security.get-task-allow bool true" ~/dummy.entitlements`
4. Sign the executable
>    `% codesign -s - -f --entitlements ~/dummy.entitlements ~/your_code`
5. Change permission of /cores, ensure 8GB+ free disk space 
>    `% sudo chmod 1777 /cores`
6. Run your code
>    `% ./your_code`
>    zsh: segmentation fault (core dumped)  ./your_code

7. Check if core file created in /cores