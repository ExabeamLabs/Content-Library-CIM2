#### Parser Content
```Java
{
Name = "atlassian-bitbucket-str-app-activity-success-sshgit"
Vendor = "Atlassian"
Product = "Atlassian BitBucket"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" | SSH - git"""
]
Fields = [
"""([^\|]*\|){4}\s*({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
"""([^\|]*\|){0}\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*\|"""
"""([^\|]*\|){3}\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""([^\|]*\|){5}\s*({action}[^\|]+?)\s*\|"""
"""([^\|]*\|){5}\s*SSH - ({operation}[^\|\']+)\s\'({object}[^\|\']+)\'"""
"""([^\|]*\|){10}\s*({additional_info}[^\|]+?)\s*\|"""
]
ParserVersion = "v1.0.0"


}
```