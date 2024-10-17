#### Parser Content
```Java
{
Name = vmware-carbonblackedr-kv-endpoint-activity-cbprotection
  Vendor = VMware
  Product = Carbon Black EDR
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Cb Protection event:""", """subtype="""", """type=""", """policy=""" ]
  Fields = [
    """({host}[\w.\-]+)\s(\-\s)+Cb Protection event:"""
    """\stext="({additional_info}[^"]+)"""",
    """\stype="({operation}[^"]+)"""",
    """\ssubtype="({event_name}[^"]+)"""",
    """\shostname="(({domain}[^"\\]+)\\)?({dest_host}[^"\\]+)"""",
    """\susername="(({domain}[^"\\]+)\\)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """\sip_address="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\spolicy="+({policy_name}[^"]+)"""",

  ]
  ParserVersion = "v1.0.0"


}
```