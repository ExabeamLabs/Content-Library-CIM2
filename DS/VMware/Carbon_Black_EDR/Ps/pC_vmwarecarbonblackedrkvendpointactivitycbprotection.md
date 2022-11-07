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
    """\susername="(({domain}[^"\\]+)\\)?({user}[^"\\]+)"""",
    """\sip_address="({dest_ip}[a-fA-F\d.:]+)""",
    """\spolicy="+({policy_name}[^"]+)"""",

  ]
  ParserVersion = "v1.0.0"


}
```