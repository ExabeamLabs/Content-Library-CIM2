#### Parser Content
```Java
{
Name = "tanium-cp-kv-alert-trigger-success-eventdetect"
Vendor = "Tanium"
Product = "Tanium Core Platform"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""" Tanium """
"""Timestamp="""
"""Computer-Name ="""
"""Computer-IP"""
]
Fields = [
"""\d\d:\d\d:\d\d\.\d+(?:\+|-)\d\d:\d\d\s+({host}[\w\-\.]+)\s+Tanium"""
"""\WTimestamp="?({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3}Z)"""
"""\WEvent-Name ="?({alert_name}[^"]+?)"?\s+([\w\-]+=|$)"""
"""\WIntel-Name ="?({alert_name}[^"]+?)"?\s+([\w\-]+=|$)"""
"""\WDetect="?({alert_type}[^"]+?)"?\s+([\w\-]+=|$)"""
"""\WIntel-Type="?({alert_type}[^"]+?)"?\s+([\w\-]+=|$)"""
"""\WPriority="?({alert_severity}[^\s"]+?)"?\s+([\w\-]+=|$)"""
"""\WEvent-Id="?({alert_id}[\w\-]+)"""
"""\WAlert-Id="?({alert_id}[\w\-]+)"""
"""\WComputer-Name ="?({src_host}[\w\-.]+)"?\s+([\w\-]+=|$)"""
"""\WComputer-IP="?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sMatch-Details=({additional_info}.+?)(\s*$|(\s\w+=))"""
"""\sMatch-Details="?\[?({additional_info}[^\]]+?)\]"\](\s*$|(\s\w+=))"""
"""\sMatch-Details.*"+user"+:"+(({domain}[^\\"]+)\\+)?({user}[\w\.\-]{1,40}\$?)(?!.*user)"+"""
"""\sMatch-Details.*"+properties"+:\{"+args"+:.*?\{"+fullpath"+:"+({process_path}(({process_dir}[^"]+)[\\/])?({process_name}[^"]+?))"+"""
"""Match-Details.*"+properties"+:\{"+args"+:"({process_command_line}.*?)","+cwd"""
]
ParserVersion = "v1.0.0"


}
```