#### Parser Content
```Java
{
Name = fortinet-fortigate-kv-configuration-modify-success-objcfg
  ParserVersion = "v1.0.0"
  Vendor = Fortinet
  Product = FortiGate
  TimeFormat = "yyyy-MM-dd 'time='HH:mm:ss"
  Conditions = [ """ type="event"""", """ subtype="objcfg"""", """ performed_on=""" ]
  Fields = [
    """date="*({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d)""",
    """\sdevname="({host}[^"]+?)"""",
    """\sdevid="({devid}[^"]+?)"""",
    """\spri="({severity}[^"]+)"""",
    """\suserfrom="(\w+\()?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\smsg="({additional_info}[^"]+?)"""",
    """\sdesc="({event_name}[^"]+)"""",
    """\suser="(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|((?i)ANONYMOUS|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\@({domain}[^"]+))?))"""",
    """\sadom="({domain}[^"])"""",
    """operation="({operation}[^"]+)"""",
    """performed_on=({object}[^"]+)"""",
    """changes="({operation_details}[^"]+)"\s*$""",
    """session_id=({session_id}\d+)"""
  ]


}
```