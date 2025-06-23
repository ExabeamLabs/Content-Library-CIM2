#### Parser Content
```Java
{
Name = fortinet-fortixdr-kv-alert-trigger-success-fortixdr
  ParserVersion = "v1.0.0"
  Vendor = Fortinet
  Product = FortiXDR
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"FortiXDR Connect LATAM 2"""" , """subtype="Security Event"""" ,"""type=event""", """action=""","""threat_name=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
    """\Wtype=({category}[^"]+)\ssubtype"""
    """\Wsubtype="({event_category}[^"]+)""""
    """device_name=({host}[^"\s]+)"""
    """operating_system="({os}[^,"]+)""""
    """process_name=({process_name}[^'\s]+)"""
    """process_path=({process_path}({process_dir}(?:[^=]+)?[\\\/])?({process_name}[^\\\/=]+))\s+\w+="""
    """\Wseverity=({alert_severity}[^"\s]+)"""
    """\Waction=({action}[^"\s]+)"""
    """mac_address=({src_mac}[^,]+)"""
    """process_hash=({process_hash}[^"\s]+)"""
    """source_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """threat_name=({alert_name}[^",\s]+)"""
    """threat_type=({alert_type}[^",\s]+)"""
  ]


}
```