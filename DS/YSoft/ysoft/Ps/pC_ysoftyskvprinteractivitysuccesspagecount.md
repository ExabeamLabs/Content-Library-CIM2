#### Parser Content
```Java
{
Name = ysoft-ys-kv-printer-activity-success-pagecount
  Vendor = YSoft
  Product = YSoft
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """DeviceName ="""",""", PrinterLocation="""",""", PageCount="""" ]
  Fields = [
    """date="({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
    """UserLogin="({user}[\w\.\-]{1,40}\$?)"""",
    """DeviceName ="({printer_name}[^"]+)"""",
    """title="({object}[^"]+)"""",
    """PageCount="({num_pages}\d+)""",
    """jobtype="({event_name}[^"]+)"""",
  ]


}
```