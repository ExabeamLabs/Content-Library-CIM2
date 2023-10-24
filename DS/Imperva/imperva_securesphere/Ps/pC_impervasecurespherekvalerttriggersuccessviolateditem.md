#### Parser Content
```Java
{
Name = "imperva-securesphere-kv-alert-trigger-success-violateditem"
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""Imperva |"""
"""violateditem="""
]
Fields = [
"""\srawuser=({db_user}[^\s]+)"""
"""\sservicename=({service_name}[^\s]+)"""
"""\sservergroup=({server_group}[^\s]+)"""
"""\salerttype=({alert_type}[^\s]+)"""
"""\sseverity=({alert_severity}[^\s]+)"""
"""\sact=(None|({action}[^\s]+))"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sspt=({src_port}\d+)"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\sdpt=({dest_port}\d+)"""
"""\ssrchostname=({src_host}[^\s]+)"""
"""\sdbname=({db_name}[^\s]+)"""
"""\sschemaname=({db_schema}[^\s]+)"""
"""\sresponsesize=({response_size}\d+)"""
"""\salertdesc=#\(({alert_name}[^\)]+)"""
"""\srawdata=#\(({db_query}[^\)]+)"""
]
DupFields = [
"db_user->account"
]
ParserVersion = "v1.0.0"


}
```