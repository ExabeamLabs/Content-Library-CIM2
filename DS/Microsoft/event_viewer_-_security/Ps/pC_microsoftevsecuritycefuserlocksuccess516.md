#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-user-lock-success-516
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|AD FS Auditing:516""" ]
  Fields = ${MicrosoftParserTemplates.cef-ad-fs-audit.Fields}[
    """\sdhost=({dest_host}[\w\-.]+?)(\s+[\w\.]+=|\s*$)""",
    """\sahost=({src_host}.+?)(\s+[\w\.]+=|\s*$)""",
    """\sdvc=({host}.+?)(\s+[\w\.]+=|\s*$)""",
    """\sdvchost=({host}.+?)(\s+[\w\.]+=|\s*$)"""
  ]

cef-ad-fs-audit = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch"
  Fields = [
    """\srt=({time}\d{13})""",
    """\sexternalId=({event_code}\d+)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sdeviceSeverity=({result}\w+)""",
    """\scs5=({email_address}[^@=\s]+@[^@=\s\-]+)""",
    """\scs5=({domain}[^\\=]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+[\w\.]+=|\s*$)""",
    """\sduser=(NETWORK SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+[\w\.]+=|\s*$)""",
    """CEF:([^\|]*\|){5}({failure_reason}[^\|]+).*Audit_failure""",
    """Audit_failure.*\scs5=[^=\-]*?-(|({failure_reason}.+?))(\s+[\w\.]+=|\s*$)""",
  
}
```