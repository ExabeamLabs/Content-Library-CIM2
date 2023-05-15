#### Parser Content
```Java
{
Name = gtb-gtbdlp-cef-file-delete-logged
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|GTB|""", """|I/O Logged|I/O Logged Violation|""", """operation=Delete from USB act=Logged""" ]
  Fields = ${GTBParsersTemplates.cef-gtb-alerts.Fields}[
    """\Wdest=Removable Media:\s+"+(?:"+|({file_dir}[^=]*?[\\\/]+)?({file_name}[^\\\/=]+?(\.({file_ext}\w+))?))"+\s+\w+=""",
    """\Wdest=Removable Media:\s+"+\s*({file_path}(?:\w:|\\|\/)[^=]+?)"+\s+\w+=""",
    """({device_type}USB)"""
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
      """\Wcs7=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\w+=""",
      """\Wact=({action}[^=]+)\s+\w+=""",
      """CEF:[^\|]+\|GTB\|(?:[^\|]+\|){2}({alert_type}[^\|]+)?\|\s*({alert_name}[^\|]+)\|({alert_severity}\d+)\|"""
    ]
    DupFields = [ "operation->event_name" 
}
```