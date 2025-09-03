#### Parser Content
```Java
{
Name = opendj-o-kv-endpoint-login-connectconn
   Vendor = OpenDJ
   Product = OpenDJ
   TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
   Conditions = [ """from=""", """to=""", """] CONNECT conn=""", """protocol=LDAP""" ]
   Fields = [
     """\[({time}\d\d\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [-\+]\d+)\]""",
     """conn=({connection_id}\d+)""",
     """from=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """to=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
     """protocol=({auth_method}[^\s]+)"""
   ]
   ParserVersion = "v1.0.0"
 

}
```