#### Parser Content
```Java
{
Name = oracle-am-cef-endpoint-authentication-accessmanager
  Vendor = Oracle
  Product = Oracle Access Management
  TimeFormat = "dd/MM/yyyy HH:mm:ss Z"
  Conditions = [ """|Oracle|""", """CEF:""", """|Access Manager|""" ]
  Fields = [
    """cs5=({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s\-\d{4})""",
    """dhost=({dest_host}.+?)\s*"*(\w+=|$)""",
    """dst=({dest_ip}[\da-fA-F.:]+)\s*"*(\w+=|$)""",
    """shost=({src_host}.+?)\s*"*(\w+=|$)""",
    """\ssrc=({src_ip}[\da-fA-F.:]+)\s*"*(\w+=|$)""",
    """duser=(uid\\=)+({user}[^,]+)""",
    """({app}Access Manager)""",
    """requestUrlFileName =({file_path}({file_dir}[^\s]+?)[\/]({file_name}[^\/\s]+?))\s*"*(\w+=|$)""",
    """CEF[^|]+\|([^|]*\|){4}({event_name}.+?)\s*\|""",
    """eventId=({event_code}\d+)\s*"*(\w+=|$)""",
    """destinationServiceName =({service_name}.+?)\s*"*(\w+=|$)""",
  ]
  ParserVersion = "v1.0.0"


}
```