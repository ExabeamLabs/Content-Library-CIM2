#### Parser Content
```Java
{
Name = qush-r-json-http-session-success-flightrisk
  Conditions = [ """reveal""", """"flightrisk"""", """"tags":""", """"jobhunting"""" ]
  Fields = ${QUSHRevealParserTemplates.qush-reveal-events.Fields} [
    """({protocol}http)""",
    """"url"+:\["+({url}[^"]+)"""",
    """"host"+:\["+({web_domain}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"

qush-reveal-events = {
    Vendor = QUSH
    Product = Reveal
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Fields = [
      """"agent_hostname"+:"+({host}[^"]+)"""",
      """"timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)"""",
      """"description"+:"+({additional_info}[^\n]+?)",""",
      """"username"+:"+((({domain}[^\",]+)\\+)?({user}[^",]+))"""",
      """"source_ip"+:\["+({src_ip}[A-Fa-f\d:.]+)"""",
      """"binary_name"+:\["+({file_name}[^",]+(\.({file_ext}[\w]+))?)"\]""",
      """"binary_path"+:"+({file_path}[^"]+)"""",
      """"anonymised_description"+:"+({event_name}[^\n]+?)",""",
      """"accountname"+:\["+((({domain}[^\",]+)\\+)?({user}[^",]+))"\]"""
    
}
```