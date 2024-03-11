#### Parser Content
```Java
{
Name = wiz-w-mix-app-notification-success-initiatedisk
 ParserVersion = "v1.0.0"
 Conditions = [ """,InitiateDiskScanContainerImage,""", """,SUCCESS""" ]
 Fields = ${wiz-system-info-events.Fields}[
   """({event_name}InitiateDiskScanContainerImage)"""
   ]


}
```