#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-share-access-endpoint-smbclient
  Conditions = [ """MSWinEventLog""", """Microsoft-Windows-SMBClient""" ]
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Event Viewer - SMB
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss yyyy"]
  Fields = [
    """\s({time}[a-zA-Z]{3} \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})"""
    """({time}\d{1,4}-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """\d+\s+({event_code}\d+)\s+Microsoft-Windows-SMBClient"""
    """({host}[\w\-\.]+)\s+None"""
    """None\s*({event_name}[^\:]+?)\s+(\w+:|Share name:)"""
    """Session ID:\s*({session_id}[^\s]+)"""
    """Status:\s*({result}[^\s]+)"""
    """Guidance:\s*({additional_info}[^:.,]+)"""
    """\s({dest_ip}((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({dest_port}\d+))?\s+[^\s]+\s+\-?\s*MSWinEventLog"""
    """Error:\s*\{({result}[^\}]+)\}"""
    """({log_name}MSWinEventLog)"""
  ]
  DupFields = [ "host->src_host" ]


}
```