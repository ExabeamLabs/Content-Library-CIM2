#### Parser Content
```Java
{
Name = cyberark-epm-json-app-activity-success-zerotouchevent
  ParserVersion = v1.0.0
  Conditions = [ """"ZeroTouchEvent":""", """"setName":"""", """"agentId":"""" ]
  Fields = ${CyberarkParsersTemplates.json-cyberark-activity.Fields} [
    """({event_name}ZeroTouchEvent)""",
  ]

json-cyberark-activity {
    Vendor = CyberArk
    Product = CyberArk Endpoint Privilege Manager
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[-+]\d\d:\d\d)""",
      """\d\d:\d\d\s({host}[^\s]+)\sLOGSTASH""",
      """"Size"+:"+({bytes}\d+)""",
      """"computerName"+:"+({src_host}[^"]+)""",
      """"Description"+:"+({additional_info}[^"]+)""",
      """"@user"+:"+(({domain}[^"\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
      """"(U|u)ser"+:"+(({domain}[^"\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
      """"Path"+:"+({process_path}({process_dir}[^"]*)\\\\({process_name}[^"]+))""",
      """"eventId"+:"+({event_code}[^"]+)""",
      """"Hash"+:"+({file_hash}[^"]+)""",
    
}
```