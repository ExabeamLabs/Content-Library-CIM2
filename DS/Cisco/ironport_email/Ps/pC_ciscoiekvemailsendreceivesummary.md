#### Parser Content
```Java
{
Name = cisco-ie-kv-email-send-receive-summary
  ParserVersion = v1.0.0    
  Vendor = Cisco
  Product = IronPort Email
  TimeFormat = "MM/dd/yyyy HH:mm:ss Z"
  Conditions = [ """ Info: MID """, """From:""", """To:""", """Subject""" ]
  Fields = [
    """\srt=({time}\d+)""",
    """({time}\w+ \d+ \d\d:\d\d:\d\d) mail_logs:""",
    """direction=({direction}[^,]+)""",
    """From:\s*<({src_email_address}[^\s@>]+@[^\s@>]+)""",
    """To:\s*<({email_recipients}({dest_email_address}[^\s@>;,]+@[^\s@>;,]+)[^>]*)""",
    """(?i)(Subject)[\s\\=]*"({email_subject}[^"]+)""",
    """({time}\d+\/\d+\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+[\+\-]\d+)""",
    """Message finished MID ({alert_id}\d+) ({result}aborted|done)""",
    """MID \d+ ready ({bytes}\d+) bytes from """,
    """AMP file reputation verdict\s*:\s*(UNKNOWN|({file_verdict}.+?))\s+\w+\s+\w+\s+\d+\s+\d+:\d+:\d+""",
    """MID\s*\d+\s*attachment\s*'({email_attachment}[^']+)""",
    """interim AV verdict using.+?({malware_score}\S+)\s+\w+\s+\w+\s+\d+\s+\d+:\d+:\d+""",
    """using engine: GRAYMAIL ({graymail_score}\S+)""",
    """CASE spam ({spam_score}\S+)""",
    """antivirus ({malware_score}\S+)""",
    """\Wfname=(|({email_attachment}.*?))\s+(\w+=|$)"""
  ]


}
```