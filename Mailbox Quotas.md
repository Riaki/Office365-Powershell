```
PS C:\Windows\system32> Get-Mailbox joe | fl "*warn*"

RecoverableItemsWarningQuota : 20 GB (21,474,836,480 bytes)
IssueWarningQuota            : 49 GB (52,613,349,376 bytes)
ArchiveWarningQuota          : 45 GB (48,318,382,080 bytes)
```

```
Set-Mailbox "joe" -IssueWarningQuota 95gb -ProhibitSendQuota 98gb -ProhibitSendReceiveQuota 99gb -UseDatabaseQuotaDefaults $false
```
