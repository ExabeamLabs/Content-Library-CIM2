#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-share-access-fail-smbserver
  Conditions = [ """MSWinEventLog""", """Microsoft-Windows-SMBServer""" ]
  ParserVersion = "v1.0.0"
  Fields = ${WindowsParsersTemplates.windows-events-share.Fields}[
    """({host}[\w\-\.]+)\s+None"""
  ]
  DupFields = [ "host->src_host" ]


}
```