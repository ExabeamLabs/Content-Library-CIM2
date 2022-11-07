#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-user-lock-success-516
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|AD FS Auditing:516""" ]

cef-ad-fs-audit = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch"
  Fields = [
    """\srt=({time}\d{13})""",
    """\sexternalId=({event_code}\d+)""",
    """\sdhost=({dest_host}.+?)(\s+[\w\.]+=|\s*$)""",
    """\sahost=({src_host}.+?)(\s+[\w\.]+=|\s*$)""",
    """\sdst=({dest_ip}[a-fA-F\d.:]+)""",
    """\sdvc=({host}.+?)(\s+[\w\.]+=|\s*$)""",
    """\sdvchost=({host}.+?)(\s+[\w\.]+=|\s*$)""",
    """\sdeviceSeverity=({result}\w+)""",
    """\scs5=({email_address}[^@=\s]+@[^@=\s\-]+)""",
    """\scs5=({domain}[^\\=]+)\\+({user}[^\\=]+?)(\s+[\w\.]+=|\s*$)""",
    """\sduser=(NETWORK SERVICE|({user}.+?))(\s+[\w\.]+=|\s*$)""",
    """CEF:([^\|]*\|){5}({failure_reason}[^\|]+).*Audit_failure""",
    """Audit_failure.*\scs5=[^=\-]*?-(|({failure_reason}.+?))(\s+[\w\.]+=|\s*$)""",
  
}
```