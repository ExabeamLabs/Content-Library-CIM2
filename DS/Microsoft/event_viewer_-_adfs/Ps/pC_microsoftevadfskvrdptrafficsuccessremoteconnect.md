#### Parser Content
```Java
{
Name = microsoft-evadfs-kv-rdp-traffic-success-remoteconnect
  Vendor = Microsoft
  Product = Event Viewer - ADFS
  ParserVersion = "v1.0.0"
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
  Conditions = [ """1149""", """Microsoft-Windows-TerminalServices-RemoteConnectionManager""", """Remote Desktop Services: """, """User authentication succeeded:"""  ]
  Fields = [
    """\s({time}\w+\s\w+\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
    """({event_code}1149)\s+Microsoft-Windows-TerminalServices-RemoteConnectionManager""",
    """Information\s+({host}[^\s]+)""",
    """({event_name}User authentication succeeded)""",
    """User:\s+(({email_address}[^\s@]+@[^\.\s]+\.[^\s]+)|({user}[\w\.\-]{1,40}\$?)@({domain}[^\s]+?)\.?|({=user}[^\s]+))\s""",
    """Domain:\s+(|({domain}[^\s]+))\s+Source Network Address:"""
    """Source Network Address:\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\d+\s"""
  ]
  DupFields = [ "host->dest_host" ]


}
```