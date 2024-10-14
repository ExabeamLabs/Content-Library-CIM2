#### Parser Content
```Java
{
Name = qush-r-json-file-write-success-filecopy
  Conditions = [ """reveal""", """"filecopy"""", """"tags":""", """"datatracking"""" ]
  Fields = ${QUSHRevealParserTemplates.qush-reveal-events.Fields} [
    """({operation}filecopy)"""
    """"target_file_name":\["({dest_file}[^"]+)""""
    """"target_file_path":\["({dest_path}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"

qush-reveal-events = {
    Vendor = NextDLP
    Product = Reveal
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSZ"]
    Fields = [
      """"agent_hostname"+:"+({host}[^"]+)"""",
      """"timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)"""",
      """"description"+:"+({additional_info}[^\n]+?)\s*",""",
      """"username":"(({full_name}[^\\\s"]+\s[^"\\]+)|(({domain}[^"\s\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
      """"destination_ip":\["({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"\]""",
      """"destination_port":\["({dest_port}\d{1,5})"\]""",
      """"source_ip":\["({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"\]""",
      """"source_port":\["({src_port}\d{1,5})"\]"""
      """"binary_path"+:"+({process_path}({process_dir}[^"]+?)\\+({process_name}[^"\\]+))"""",
      """"binary_name"+:\["+({process_name}[^",]+)"\]""",
      """"anonymised_description"+:"+({event_name}[^\n]+?)",""",
      """"accountname"+:\["+((({domain}[^\\",]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"\]""",
      """"file_name":\["({file_name}[^"]+?(\.({file_ext}[^"\.:]+)(:[^"]+)?)?)"""",
      """"file_path":\["({file_path}[^"]+)"""",
      """"tags":\[[^\]]*?"({tag}[^"\]]+)"\]""",
      """"agent_hostname":"({host}[\w\-\.]+)"""",
      """"created_by":"policy:[^"]+?name=({event_name}[^"]+)""""
    
}
```