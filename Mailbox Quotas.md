```
PS C:\Windows\system32> Get-Mailbox joe | fl "*warn*"

RecoverableItemsWarningQuota : 20 GB (21,474,836,480 bytes)
IssueWarningQuota            : 49 GB (52,613,349,376 bytes)
ArchiveWarningQuota          : 45 GB (48,318,382,080 bytes)
```

```
Set-Mailbox "joe" -IssueWarningQuota 95gb -ProhibitSendQuota 98gb -ProhibitSendReceiveQuota 99gb -UseDatabaseQuotaDefaults $false
```

```
Get-Mailbox tommy | fl "*quota*"


ProhibitSendQuota            : 98 GB (105,226,698,752 bytes)
ProhibitSendReceiveQuota     : 99 GB (106,300,440,576 bytes)
RecoverableItemsQuota        : 30 GB (32,212,254,720 bytes)
RecoverableItemsWarningQuota : 20 GB (21,474,836,480 bytes)
CalendarLoggingQuota         : 6 GB (6,442,450,944 bytes)
UseDatabaseQuotaDefaults     : False
IssueWarningQuota            : 95 GB (102,005,473,280 bytes)
RulesQuota                   : 256 KB (262,144 bytes)
ArchiveQuota                 : 100 GB (107,374,182,400 bytes)
ArchiveWarningQuota          : 90 GB (96,636,764,160 bytes)
```
