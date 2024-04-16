#### Parser Content
```Java
{
Name = "ibm-guardium-cef-alert-trigger-success-loginfail"
Vendor = "IBM"
Product = "Guardium"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|IBM|Guardium|"""
"""DatabaseName ="""
"""DBUser="""
]
Fields = [
"""\|IBM\|Guardium\|[^|]+\|({alert_name}[^|]+)"""
"""Severity=({alert_severity}[^=]+?)(?:\s*\w+=|\s*$)"""
"""Category=({alert_type}[^=]+?)(?:\s*\w+=|\s*$)"""
"""DatabaseName =({db_name}[^=]+?)(?:\s*\w+=|\s*$)"""
"""DBUser=\s*(?:|(({domain}[^\\=]+)\\+)?({db_user}[^=\\\/]+?))(?:\s*\w+=|\s*$)"""
"""ServerIP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""ServerHostname=({host}[^=]+?)(?:\s*\w+=|\s*$)"""
"""ServerType=({server_group}[^=]+?)(?:\s*\w+=|\s*$)"""
"""ClientIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""rt=({time}\d{13})"""
"""OSUser=\s*(?:|(({domain}[^\\=]+)\\+)?({user}[\w\.\-]{1,40}\$?))(?:\s*\w+=|\s*$)"""
"""AlertDetails=(\s+|({db_query}[^$]+?))(?:\s*\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```