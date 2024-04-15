#### Parser Content
```Java
{
Name = "sailpoint-securityiq-csv-file-operation"
Vendor = "Sailpoint"
Product = "SecurityIQ"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions=["""action type""", """object name""", """samaccountname""", """creation_timestamp""", """application type""" ]
 Fields=[
   """creation_timestamp\\"+:\\"+({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d{3})""",
   """message"+:\s*"+[^\s]+\s+({host}[^\s]+)""",
   """"+samaccountname\\"+:\\"+({user}[^\\"]+)""",
   """"+userprincipalname\\"+:\\"+({email_address}[^\\"]+)""",
   """"+object name\\"+:\\"+({file_name}[^\\"]+)""",
   """"+file extension\\"+:\\"+({file_ext}[^\\"]+)""",
   """"+ip address\\"+:\\"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
   """"+domain\\"+:\\"+({domain}[^\\"]+)""",
   """"+application type\\"+:\\"+({app}[^\\"]+)""",
   """"+path\\"+:\\"+\\+({path}[^"]+)\\"+""",
   """"+action type\\"+:\\"+({operation}[^\\"]+)"""
 ]
ParserVersion = "v1.0.0"


}
```