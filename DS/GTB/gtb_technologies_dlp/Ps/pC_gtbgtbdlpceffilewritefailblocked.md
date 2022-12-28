#### Parser Content
```Java
{
Name = gtb-gtbdlp-cef-file-write-fail-blocked
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|GTB|""", """|| Violation|""", """operation=Save to CD/DVD act=Blocked""" ]
  Fields = ${GTBParsersTemplates.cef-gtb-alerts.Fields}[
    """\Wrt=({time}\d{13})""",
    """\Wdest=Removable Media:\s+"+(?:"+|({file_dir}[^=]*?[\\\/]+)?({file_name}[^\\\/=]+?(\.({file_ext}\w+))?))"+\s+\w+=""",
    """\Wdest=Removable Media:\s+"+\s*({file_path}(?:\w:|\\|\/)[^=]+?)"+\s+\w+=""",
    """({device_type}CD\/DVD)"""
  ]

cef-gtb-alerts = {
    Vendor = GTB
    Product = GTB Technologies DLP
    TimeFormat = "epoch"
    Fields = [
      """\w+\s\d\d\s\d\d:\d\d:\d\d\s+({host}[\w-]+)""",
      """\Wrt=({time}\d{13})""",
      """\Wuser=({full_name}(({last_name}[^,=]+),\s+({first_name}[^=\(]+)\s+[^=]+|[^=]+))\s+\w+=""",
      """\Wcs5=({user}[^=]+)\s+\w+=""",
      """\Wcs6=({email_address}[^=@]+@[^=]+)\s+\w+=""",
      """\|GTB\|({dest_host}[^\|]+)\|""",
      """\Woperation=({operation}[^=]+)\s+\w+=""",
      """\WdeviceExternalId=({device_id}[^=]+)\s+\w+=""",
      """\Wcs7=({src_ip}[[A-Fa-f\d:.]+)\s+\w+=""",
      """\Wact=({action}[^=]+)\s+\w+=""",
      """CEF:[^\|]+\|GTB\|(?:[^\|]+\|){2}({alert_type}[^\|]+)?\|\s*({alert_name}[^\|]+)\|({alert_severity}\d+)\|"""
    ]
    DupFields = [ "operation->event_name" 
}
```