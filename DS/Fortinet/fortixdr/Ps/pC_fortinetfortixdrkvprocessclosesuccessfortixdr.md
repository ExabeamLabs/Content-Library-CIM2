#### Parser Content
```Java
{
Name = fortinet-fortixdr-kv-process-close-success-fortixdr
  ParserVersion = "v1.0.0"
  Vendor = Fortinet
  Product = FortiXDR
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"FortiXDR Connect LATAM 2"""", """sub_system=""" , """type=event""" , """devid=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
    """\Wtype=({category}[^"]+)\ssubtype"""
    """\Wsubtype="({event_category}[^"]+)""""
    """device_name=({host}[^"\s]+)"""
    """description="({description}[^"]+)""""
    """from device \[({host}[\w\-.]+)"""
  ]


}
```