#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-service-create-success-4697-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSZ" ]
Conditions = [ """ Event ID:4697 """, """A service was installed in the system""", """ Computer_name:""" ]
Fields = [
  """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3}Z)""",
  """({event_code}4697)""",
  """({event_name}A service was installed in the system)""",
  """\sComputer_name:({dest_host}({host}[\w\-.]+))\s""",
  """Subject:.*?Security ID:\s*(|({user_sid}.+?))(\\[nrt]\s+|\s*)Account Name:\s*(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\\[nrt]\s+|\s*)Account Domain:\s*(|({domain}.+?))(\\[nrt]\s+|\s*)Logon ID:\s*(|({login_id}[^\s]+?))((\\[nrt])+\s*|\s*)Service Information:""",
  """\sService Name:\s*(|({service_name}[^:]+?)(_[0-9a-f]+)?)(\s|\\[rnt])""",
  """\sService File Name:\s*((?-i)\\+[rnt]\\*)*({service_command_line}({process_command_line}[^=]+?))(\s|\\[rnt])+Service Type:""",
  """\sService File Name:\s*\"*(|({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}[^\\\/\"]+?)))\"*\s"""
  """\sService Type:\s*({service_type}.+?)(\\[rnt]\s+|\s)""",
  """\sService Start Type:\s*({service_start_type}.+?)(\\[rnt]\s+|\s)""",
  """\sService Account:\s*(({account_domain}[^\\"\s]+)\\)?((?-i)\\+[rnt])*({account_name}[^"\s]+)"""
]
ParserVersion = "v1.0.0"


}
```