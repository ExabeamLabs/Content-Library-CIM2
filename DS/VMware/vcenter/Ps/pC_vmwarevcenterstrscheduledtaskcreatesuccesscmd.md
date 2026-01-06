#### Parser Content
```Java
{
Name = "vmware-vcenter-str-scheduled-task-create-success-cmd"
Vendor = "VMware"
Product = "vCenter"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
Conditions = [
""" CMD """
""" CROND """
]
Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+([\+\-]\d\d:\d\d|Z))"""
    """\d\d:\d\d:\d\d(\.\S+)?\s+({host}[\w\-.]+)\s+CROND""",
    """\((({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\) CMD""",
    """\sUSER\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s""",
    """\sCMD\s+\(\s*({task_name}[^\)]+?)\s*\)""",
    """\sCMD\s+({process_command_line}.+?)\s*$""",
    """\sCMD\s\(([\.\w\-]+\s)?({process_path}(\/[^\/\)\s]+)+)(\s|\))"""
]
ParserVersion = "v1.0.0"


}
```