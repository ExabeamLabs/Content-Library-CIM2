#### Parser Content
```Java
{
Name = fortinet-fortigate-kv-app-activity-wireless
  ParserVersion = "v1.0.0"
  Vendor = Fortinet
  Product = FortiGate
  TimeFormat = "yyyy-MM-dd 'time='HH:mm:ss"
  Conditions = [ """type="event"""", """subtype="wireless"""" ]
  Fields = [
    """date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d)""",
    """\slogdesc="*({event_name}[^\s"]*)"*""",
# sn is removed
    """\sap="*({ap}[^\s"]*)"*""",
# radioid is removed
# radioid is removed
# noise is removed
    """\smsg="*({additional_info}[^\s"]*)"*""",
# radioband is removed
# stamac is removed
  ]


}
```