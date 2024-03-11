#### Parser Content
```Java
{
Name = unix-unix-mix-user-switch-success-sudo
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
"""sudo:""",
"""; USER""",
"""; COMMAND"""
  ]
  Fields = [
"""({time}\w{3} \d{1,2}, \d\d\d\d, \d{1,2}:\d{1,2}:\d{1,2} (?i)(am|pm))""",
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
"""\"timestamp\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
"""\"agent_hostname\":\"({host}[^\"]+)\"""",
"""\"agent_hostname\":\"(({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|({dest_host}[^\"]+))\"""",
"""({host}[\w\.\-]+)?:?\s*sudo:""",
"""\"agent\":\{\"id\":\"({agent_id}\d+)\"""",
"""\"agent\":\{\"name\":\"[^\"]*\",\"id\":\"({agent_id}\d+)\"""",
"""({event_code}sudo):\s+(?:\[[^]]+\])?\s*(({domain}[^\\:;]+)\\+)?({user}[^\s:]+).+?USER\\*=({dest_user}[^;\s]+)""",
"""\/(user(add|del)|passwd)\s([^"]*?\s*)?({dest_user}\w+?)\s*(\d\d\d\d\-|$)""",
"""\WPWD\\?=({process_dir}[^\s;]+)""",
"""\WCOMMAND\\?=({process_path}([^\s]+[\\\/]+)?({process_name}[^;\\\/\s]+))\s(?:|;|$)""",
"""\WCOMMAND\\?=({process_command_line}[^;\"]+)(\"|\s(?:|;|$))""",
"""\"description\":\"({event_name}[^\"]+)\"""",
"""\"level\":({level}[^\",]+)""",
"""\"groups\":\[({groups}[^\]]+)""",
"""\"pci_dss\":\[({pci_dss}[^\]]+)""",
"""\"cluster\":\{[^\{\}]+?\"name\":\"({cluster_name}[^\"]+)\"""",
"""\"host\":\"({wazuh_manager}[^\"]+)\"""",
"""\/group(add|del)\s({group_name}[^"]+?)\s*(\d\d\d\d\-|$)"""
  ]
  DupFields= ["dest_user->account", "host->dest_host"]


}
```