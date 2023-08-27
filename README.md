Get-Acl -Path hklm:\System\CurrentControlSet\services\regsvc | fl

If we have full control of a registry key in this path, we can compile a malicious executable written in .c and make that executable run a command. I.e add users to a group, run a reverse shell etc.

If you notice NT AUTHORITY\INTERACTIVE Allow FullControl that means everyone has access to that service.

You can modify the windows_dll.c and windows_service.c to generate your payload.
