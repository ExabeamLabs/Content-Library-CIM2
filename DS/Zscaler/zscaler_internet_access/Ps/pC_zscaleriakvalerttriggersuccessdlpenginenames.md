#### Parser Content
```Java
{
Name = "zscaler-ia-kv-alert-trigger-success-dlpenginenames"
Vendor = "Zscaler"
Product = "Zscaler Internet Access"
TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
Conditions = [
"""dlpenginenames="""
"""login="""
"""recordid="""
"""company="""
]
Fields = [
"""dlpdictnames=({alert_name}[^=]+?)\s*\w+="""
"""lastmodtime=({time}\w+ \w+\s*\d{1,2}\s*\d+:\d+:\d+\s*\d+)"""
"""dlpdictnames=(None|({dlp_dict}[^=]+?))\s*\w+="""
"""dept=(-|({department}[^=]+?))\s*\w+="""
"""applicationname=(None|({app}[^=]+?))\s*\w+="""
"""filename=(None|({file_name}[^=]+?))\s*\w+="""
"""filesource=({additional_info}[^=]+?)\s*\w+="""
"""filemd5=(None|({hash_md5}[^=]+?))\s*\w+="""
"""login=(({email_address}[^@]+@[^\.]+\.[^=]+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\w+="""
"""policy=(None|({policy_name}[^=]+?))\s*\w+="""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```