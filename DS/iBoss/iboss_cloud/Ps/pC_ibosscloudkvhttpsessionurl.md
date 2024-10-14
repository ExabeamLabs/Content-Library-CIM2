#### Parser Content
```Java
{
Name = "iboss-cloud-kv-http-session-url"
Vendor = "iBoss"
Product = "Iboss Cloud"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
""",URL_LOG_ENTRY,"""
""",URL_LOG_ID="""
""",IBOSS="""
""",URL="""
""",BYTES="""
]
Fields = [
"""({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s((?i)AM|PM))"""
"""IBOSS=({host}[\w\-.]+),"""
"""URL=({url}(\w+:\/\/)?({web_domain}[^\/]+?)({uri_path}\/[^\?]*?)?({uri_query}\?[^,]+)?)(,|")"""
"""CATEGORIES_NAMES=({categories}({category}[^,;\=]+)[^\=]*?),\w+="""
"""ACTION=({action}[^,]+),"""
"""SRC_IPADDR=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,"""
"""COMP_NAME=({src_host}[\w\-.]+),"""
"""USER=(({email_address}[^@=]+@[^.]+\.[^,\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""REQUEST_METHOD=({method}[^,]+),"""
"""USER_AGENT=({user_agent}[^=]+?),\w+="""
"""CONTENT_TYPE=({mime}[^,]+),"""
"""BYTES=({bytes_out}\d+)"""
]
ParserVersion = "v1.0.0"


}
```