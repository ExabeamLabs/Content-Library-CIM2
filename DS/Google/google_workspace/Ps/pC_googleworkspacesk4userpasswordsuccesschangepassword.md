#### Parser Content
```Java
{
Name = "google-workspace-sk4-user-password-success-changepassword"
Vendor = "Google"
Product = "Google Workspace"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""CHANGE_PASSWORD""""
"""destinationServiceName =Google Apps"""
""""USER_SETTINGS""""
]
Fields = [
""""time"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""""
"""({event_name}CHANGE_PASSWORD)"""
""""ipAddress"\s*:\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""email"\s*:\s*"({email_address}[^"@]+?@[^"]+?)""""
""""name"\s*:\s*"USER_EMAIL"[^"]*"value"\s*:\s*"({dest_email_address}[^"@]+@[^"]+)"""",
"""destinationServiceName =({app}[^=]+?)\s*(\w+=|$)"""
]
DupFields = [ "dest_email_address->dest_user" ]
ParserVersion = "v1.0.0"


}
```