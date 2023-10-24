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
    """\ssrcip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sport=({src_port}\d+)""",
    """\smsg="({additional_info}[^"]+?)"""",
    """\ssaddr="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\suser="(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|((?i)ANONYMOUS|({user}[\w\.\-]{1,40}\$?)(\@({domain}[^"]+))?))""""
  ]


}
```