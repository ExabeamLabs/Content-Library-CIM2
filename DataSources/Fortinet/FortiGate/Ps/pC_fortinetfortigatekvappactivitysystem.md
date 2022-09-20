#### Parser Content
```Java
{
Name = fortinet-fortigate-kv-app-activity-system
  ParserVersion = "v1.0.0"
  Vendor = Fortinet
  Product = FortiGate
  TimeFormat = "yyyy-MM-dd 'time='HH:mm:ss"
  Conditions = [ """type="event"""", """subtype="system"""" ]
  Fields = [
    """date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d)""",
    """\sdevname="({host}[^"]+?)"""",
    """\sdevid="({devid}[^"]+?)"""",
# logid is removed
# vd is removed
    """\scommunity="({community}[^"]+?)"""",
    """\sversion="({version}[^"]+?)"""",
    """\slevel="({alert_severity}[^"]+?)"""",
    """\slogdesc="({alert_name}[^"]+?)"""",
    """\ssrcip=({src_ip}[a-fA-F\d.:]+)""",
    """\sport=({src_port}\d+)""",
    """\smsg="({additional_info}[^"]+?)"""",
  ]


}
```