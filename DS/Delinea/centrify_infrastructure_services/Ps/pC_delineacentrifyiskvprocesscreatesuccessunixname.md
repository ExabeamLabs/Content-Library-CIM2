#### Parser Content
```Java
{
Name = delinea-centrifyis-kv-process-create-success-unixname
  Vendor = Delinea
  Product = Centrify Infrastructure Services
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """ MachineName: """", """ UnixName: """", """Command:""" ]
  Fields = [
    """Time:\s*"+({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d\.\d+)""",
    """MachineName:\s*"+({host}[\w\-.]+)""",
    """Command:\s*"+({process_command_line}[^"]+)""",
    """Command:\s*"+({process_path}({process_dir}[^\s"]*?)[\\\/]*({process_name}[^\\\/\s"]+))""",
    """UserName:\s*"+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))""",
    """UnixName:\s*"+({account}[^"]+)""",
    """ClientName:\s*"+(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^"]+))""",
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```