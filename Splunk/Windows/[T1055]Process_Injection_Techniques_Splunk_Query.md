```
index=sysmon (
    (EventCode=10 AND (GrantedAccess="*0x1F0FFF*" OR GrantedAccess="*0x1fffff*" OR GrantedAccess="*0x1410*" OR GrantedAccess="*0x143a*"))
    OR
    (EventCode=8)
)
| table _time, host, EventCode, SourceImage, TargetImage, GrantedAccess, User, CommandLine
```