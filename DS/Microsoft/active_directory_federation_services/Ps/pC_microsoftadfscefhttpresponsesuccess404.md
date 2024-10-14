#### Parser Content
```Java
{
Name = microsoft-adfs-cef-http-response-success-404
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """|AD FS Auditing:404""" ]

cef-ad-fs-audit = {
  Vendor = Microsoft
  Product = Active Directory Federation Services
  TimeFormat = "epoch"
  Fields = [
    """\srt=({time}\d{13})""",
    """\sexternalId=({event_code}\d+)""",
    """\sdhost=({dest_host}.+?)(\s+[\w\.]+=|\s*$)""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sdvc=({host}.+?)(\s+[\w\.]+=|\s*$)""",
    """\sdvchost=({host}.+?)(\s+[\w\.]+=|\s*$)""",
    """\sdeviceSeverity=({result}\w+)""",
    """\scs5=({email_address}[^@=\s]+@[^@=\s\-]+)""",
    """\scs5=({domain}[^\\=]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+[\w\.]+=|\s*$)""",
    """\sduser=(NETWORK SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+[\w\.]+=|\s*$)""",
    """CEF:([^\|]*\|){5}({failure_reason}[^\|]+).*Audit_failure""",
    """Audit_failure.*\scs5=[^=\-]*?-(|({failure_reason}.+?))(\s+[\w\.]+=|\s*$)""",
  
}
```