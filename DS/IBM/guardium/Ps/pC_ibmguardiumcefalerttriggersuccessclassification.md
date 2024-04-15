#### Parser Content
```Java
{
Name = "ibm-guardium-cef-alert-trigger-success-classification"
Vendor = "IBM"
Product = "Guardium"
TimeFormat = "epoch"
Conditions = [
"""|IBM|Guardium|"""
"""cs3Label=Classification"""
"""Alert|"""
]
Fields = [
"""\|rt=({time}\d{13})"""
"""\ssuser=(:\w+=)?(?:|({user}.+?))\s*\w+="""
"""\sduser=([^\\=]+\\+)?(?:|({db_user}.+?))\s*\w+="""
"""\scs2=({server_group}.+?)\s*\w+="""
"""\ssrc=(?!0\.0\.0\.0)({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sdst=(?!0\.0\.0\.0)({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""CEF.+?([^|]+\|){5}[\s-]*({alert_name}.+?)[\s-]*(Alert)?\s*\|"""
"""CEF.+?([^|]+\|){6}({alert_severity}[^|]+)"""
]
DupFields = [
"alert_name->alert_type"
"db_user->account"
]
ParserVersion = "v1.0.0"


}
```