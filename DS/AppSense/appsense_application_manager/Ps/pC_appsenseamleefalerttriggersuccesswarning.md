#### Parser Content
```Java
{
Name = "appsense-am-leef-alert-trigger-success-warning"
Vendor = "AppSense"
Product = "AppSense Application Manager"
TimeFormat = ["MM/dd/yyyy hh:mm:ss a","M/dd/yyyy hh:mm:ss a"]
Conditions = [
"""AppSense Application Manager"""
"""SourceName ="""
"""Message="""
"""EventCode="""
]
Fields = [
"""({time}\d+/\d+/\d+ \d+:\d+:\d+ (am|AM|pm|PM))"""
"""ComputerName =({dest_host}[^\s]+)"""
"""Sid=({dest_user_sid}[^\s]+)"""
"""\s+Type=({alert_severity}[^\s]+)"""
"""\'\w+:\\+(?i)users\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""Hash:(({hash_sha256}\w{64})|({hash_sha1}\w{40})|({hash_md5}\w{32}))"""
"""Vendor:\s+({process_vendor}[^\]]+)"""
"""Message=AppSense Application Manager ({alert_name}.+?)\s+(of [^\w]|\'|for)"""
"""Message=(The file )?\'.+?\'( has had)?\s+({alert_name}.+?)\s*(\.|of|for)"""
"""Message=\'(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\'"""
"""\'({process_path}({process_dir}(?:(\w+:)*([\\\/]+[^\\\/'\]\"]+)+)?[\\\/]+)({process_name}[^\\\/\"\]]*?))(\s+\[\w+:|')"""
]
DupFields = [
"process_path->path"
"dest_host->host"
"alert_name->alert_type"
"user_sid->account_id"
]
ParserVersion = "v1.0.0"


}
```