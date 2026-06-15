#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-certificate-create-success-4887
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "epoch", "MMM dd HH:mm:ss", "MMM dd HH:mm:ss yyyy" ]
  ParserVersion = v1.0.0
  Conditions = [ """ 4887 """, """Microsoft-Windows-Security-Auditing""" , """Certificate Services approved a certificate request""" , """MSWinEventLog """ ]
  Fields = [
    """({event_name}Certificate Services approved a certificate request)""",
    """({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+({event_code}\d+)""",
    """\d{4}\s+({event_code}4887)\s+Microsoft-Windows-Security-Auditing""",
    """\d+:\d+\s+({host}[\w\-.]+)\s+MSWinEventLog""",
    """ Requester:\s+(({domain}[^<\\\s]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """ Attributes:\s+({attributes}[^"]+)\s+Disposition""",
    """ Disposition:\s+({disposition}\d+)""",
    """ Subject:\s+({client_cert_subject}[^\s]+)"""
  ]


}
```