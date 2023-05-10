#### Parser Content
```Java
{
Name = qush-r-json-file-write-success-datacompression
  Conditions = [ """reveal""", """"zip"""", """"tags":""", """"datacompression"""" ]
  Fields = ${QUSHRevealParserTemplates.qush-reveal-events.Fields} [
    """({operation}datacompression)"""
  ]
  ParserVersion = "v1.0.0"

qush-reveal-events = {
    Vendor = QUSH
    Product = Reveal
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Fields = [
      """"agent_hostname"+:"+({host}[^"]+)"""",
      """"timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)"""",
      """"description"+:"+({additional_info}[^\n]+?)\s*",""",
      """"username":"(({full_name}[^\\\s"]+\s[^"\\]+)|(({domain}[^"\s\\]+)\\+)?({user}[^"\s]+))"""",
      """"destination_ip":\["({dest_ip}[a-fA-F\d:\.]+)"\]""",
      """"destination_port":\["({dest_port}\d{1,5})"\]""",
      """"source_ip":\["({src_ip}[a-fA-F\d:\.]+)"\]""",
      """"source_port":\["({src_port}\d{1,5})"\]"""
      """"binary_path"+:"+({process_path}({process_dir}[^"]+?)\\+({process_name}[^"\\]+))"""",
      """"binary_name"+:\["+({process_name}[^",]+)"\]""",
      """"anonymised_description"+:"+({event_name}[^\n]+?)",""",
      """"accountname"+:\["+((({domain}[^\\",]+)\\+)?({user}[^",]+))"\]""",
      """"file_name":\["({file_name}[^"]+?(\.({file_ext}[^"\.:]+)(:[^"]+)?)?)"""",
      """"file_path":\["({file_path}[^"]+)"""",
      """"tags":\[[^\]]*?"({tag}[^"\]]+)"\]""",
      """"agent_hostname":"({host}[\w\-\.]+)"""",
      """"created_by":"policy:[^"]+?name=({event_name}[^"]+)""""
    
}
```