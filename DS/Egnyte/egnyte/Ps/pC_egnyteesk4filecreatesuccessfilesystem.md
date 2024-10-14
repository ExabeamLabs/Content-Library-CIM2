#### Parser Content
```Java
{
Name = "egnyte-e-sk4-file-create-success-filesystem"
  Vendor = "Egnyte"
  Product = "Egnyte"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """destinationServiceName =Egnyte""", """"data":""", """"action":""", """"type":"file_system"""" ]
  Fields = [
    """"timestamp"\s*:\s*"({time}[^"]+)""""
    """\Wsuser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
    """"type"\s*:\s*"({file_type}[^"]+)""""
    """"action"\s*:\s*"({operation}[^"]+)""""
    """"data"\s*:.*?"target_path"\s*:\s*"({file_path}({file_dir}[^']*?[\\\/]+)?({file_name}[^'\\\/]+?(\.({file_ext}\w+))?))""""
    """"object_detail"\s*:\s*"({file_url}[^"]+)""""
    """"data"\s*:.*?"source_path"\s*:\s*"({src_file_path}({src_file_dir}[^']*?[\\\/]+)?({src_file_name}[^'\\\/]+?(\.({src_file_ext}\w+))?))""""
  ]
  ParserVersion = "v1.0.0"


}
```