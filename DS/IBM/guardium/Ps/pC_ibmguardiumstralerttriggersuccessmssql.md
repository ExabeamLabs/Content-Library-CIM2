#### Parser Content
```Java
{
Name = "ibm-guardium-str-alert-trigger-success-mssql"
Vendor = "IBM"
Product = "Guardium"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Alert based on rule ID"""
"""Database Name:"""
"""Protocol Version:"""
]
Fields = [
"""Session start:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""\w+\s+\d{1,2} \d{1,2}:\d{1,2}:\d{1,2}\s*({host}[\w\.-]+)"""
"""rule ID\s*({alert_name}.+?)\s*([#\d\\n]+)?([\w\s]+:)"""
"""rule ID\s*({alert_name}.+?)\s*-\s*Severity"""
"""Severity\s*({alert_severity}[^\s]+)\s"""
"""Category:\s*({alert_type}\S+)\s*Classification:"""
"""SQL:\s*({additional_info}.+?)?\s*SQL"""
"""Client:\s*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*(\((\()?({src_host}[\w\d\\]+)\))?"""
"""Server:\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s*(\(({dest_host}[\w\d\\]+)\))?"""
"""Server Type:\s*({server_group}.+?)\s([#\d\\n]+)?Client:"""
"""DB User:\s*(({domain}\w+)\\)?({db_user}[\w\d]+)(\s+\(.+?\))?([#\d\\n]+)?([\w\s]+:)"""
"""OS User:\s*({user}.+?)\s*([#\d\\n]+)?([\w\s]+:)"""
"""Source Program:\s*({process_path}({process_dir}.+)[\\\/]({process_name}.+?))\s([#\d\\n]+)?SQL:"""
"""Database Name:\s+({db_name}.+?)\s+([#\d\n]+)?([\w\s]+:)"""
]
DupFields = [
"db_user->account"
]
ParserVersion = "v1.0.0"


}
```