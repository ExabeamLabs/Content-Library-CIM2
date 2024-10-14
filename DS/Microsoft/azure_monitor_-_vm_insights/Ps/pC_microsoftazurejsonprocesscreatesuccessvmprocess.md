#### Parser Content
```Java
{
Name = microsoft-azure-json-process-create-success-vmprocess
    ParserVersion = v1.0.0
    Vendor = Microsoft
    Product = Azure Monitor - VM Insights
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      """"Type":"VMProcess"""",
      """ExecutableName"""
    ]
    Fields = [
"""\"TimeGenerated\":\"({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
"""Computer\"+:\"+({host}[^\"]+)"""
"""Machine\"+:\"+({src_host}[^\"]+)"""
"""ExecutableName\"+:\"+({process_name}[^\"]+)"""
"""FirstPid\"+:({process_id}\d+)"""
"""\"ExecutablePath\":\"({process_path}((|({process_dir}[^\"]*?))[\\/]+)?({process_name}[^\"\\/]+?))\s*\""""
"""CommandLine\":\"\s*({process_command_line}[^\n]+?)\s*\",\"\w+\""""
"""UserName\"+:\"+((?i)SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""UserDomain\"+:\"+({domain}[^\"]+)"""
]
DupFields = [ "process_dir->process_path_directory" ]


}
```