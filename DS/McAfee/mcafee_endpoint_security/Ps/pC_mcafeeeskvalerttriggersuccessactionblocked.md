#### Parser Content
```Java
{
Name = "mcafee-es-kv-alert-trigger-success-actionblocked"
Vendor = "McAfee"
Product = "McAfee Endpoint Security"
TimeFormat = "MM/dd/yyyy        hh:mm:ss a"
Conditions = [
"""\tAction blocked"""
"""\tWould be blocked by Access Protection rule """
]
Fields = [
"""({time}\d+\/\d+\/\d+\t\d+:\d+:\d+ (am|AM|pm|PM))\t({alert_name}[^\t]+?)\s*\t(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*\t({process_path}({process_dir}[^\t]+?)({process_name}[^\\\t]+))\s*\t"""
"""\t({alert_type}[^\t]+?)\s*$"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```