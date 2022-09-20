#### Parser Content
```Java
{
Name = f5-waf-json-process-create-success-cmd
  Conditions = [ """"log_type":"WAF"""", """"log_vendor":"f5"""", """ CMD """, """]: (""" ]
  Fields = ${F5ParsersTemplates.f5-waf-activity.Fields} [
    """\(({user}[^\}\s]+)\) CMD""",
    """\sCMD \(\s*({process_command_line}[^\)]+)\)""",
    """\sCMD \(\s*[^\/]*?({process_path}({process_dir}\/[^\)]*?)({process_name}[^\/]*?[^\\]))((\\\\)*\s|\))"""
  ]
  ParserVersion = "v1.0.0"

f5-waf-activity = {
    Vendor = F5
    Product = F5 Advanced Web Application Firewall (WAF)
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """"host":"(::ffff:)?({host}[^"]+})""",
      """\d\d:\d\d:\d\d ({host}\S+)? \w+ \w+\[""",
      """\ssshd\[\d+\]:\s*({additional_info}[^",]+)"""
    
}
```