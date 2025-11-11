#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-share-access-fail-smbserver
  Product = Event Viewer - SMB
  Conditions = [ """MSWinEventLog""", """Microsoft-Windows-SMBServer""" ]
  ParserVersion = "v1.0.0"
  Fields = ${WindowsParsersTemplates.windows-events-share.Fields}[
    """Client Address(:|=)\s*(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """User Name:\s*(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*Session ID"""
    """\s({dest_ip}((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({dest_port}\d+))?\s+[^\s]+\s+\-?\s*MSWinEventLog"""
    """({host}[\w\-\.]+)\s+None"""
  ]
  DupFields = [ "host->src_host" ]


}
```