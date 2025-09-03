#### Parser Content
```Java
{
Name = unix-unix-mix-user-switch-success-sudo
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","MMM dd HH:mm:ss"]
  Conditions = [
"""sudo:""",
"""; USER""",
"""; COMMAND"""
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?""",
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+\[({=host}\w+)\]"""
"""({time}\w+\s\d+(\s|T)\d\d:\d\d:\d\d)(\.?\S+)?\s({host}[\w\.\-]+)?:?\s*sudo:""",
"""({time}\w{3} \d{1,2}, \d\d\d\d, \d{1,2}:\d{1,2}:\d{1,2} (?i)(am|pm))""",
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
"""\"timestamp\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
"""\"agent_hostname\":\"({host}[^\"]+)\"""",
"""\"agent_hostname\":\"(({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})|({dest_host}[^\"]+))\"""",
"""\s({host}[\w\.\-]+)?:?\s*sudo:""",
"""\"agent\":\{\"id\":\"({agent_id}\d+)\"""",
"""\"agent\":\{\"name\":\"[^\"]*\",\"id\":\"({agent_id}\d+)\"""",
"""({event_code}sudo):\s+(?:\[[^]]+\])?\s*(({domain}[^\\:;]+)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)).+?USER\\*=({dest_user}[^;\s]+)""",
"""\/(user(add|del)|passwd)\s([^"]*?\s*)?({dest_user}\w+?)\s*(\d\d\d\d\-|$)""",
"""\WPWD\\?=({current_working_dir}[^\s;]+)""",
"""\WCOMMAND\\?=({process_relative_path}({process_relative_dir}[^\s]+[\\\/]+)?({process_name}[^;\\\/\s]+))\s(?:|;|$)""",
"""\WCOMMAND\\?=({process_command_line}[^\"]+)(\"|$|\s(?:|;|$))""",
"""\"description\":\"({event_name}[^\"]+)\"""",
"""\"level\":({severity}[^\",]+)""",
"""\"groups\":\[({group_info}[^\]]+)""",
"""\"pci_dss\":\[({pci_dss}[^\]]+)""",
"""\"cluster\":\{[^\{\}]+?\"name\":\"({cluster_name}[^\"]+)\"""",
"""\"host\":\"({wazuh_manager}[^\"]+)\"""",
"""\/group(add|del)\s({group_name}[^"]+?)\s*(\d\d\d\d\-|$)"""
  ]
  DupFields= ["dest_user->account", "host->dest_host"]


}
```