#### Parser Content
```Java
{
Name = wiz-w-csv-user-delete-success-deleteuser
 Vendor = Wiz
 Product = Wiz
 ParserVersion = v1.0.0
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
 Conditions = [ """,DeleteUser,""", """,USER_ACCOUNT,""", """,SUCCESS""" ]
 Fields = [
   """ACCOUNT,({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6}Z)""",
   """({event_name}DeleteUser)""",
   """DeleteUser,[^}]+?"id"+:[^}]+\|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"+\}""",
   """,({email_address}[^@\s\|]+@[^\s"]+?),USER_ACCOUNT""",
   """\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.[^,]+,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,"?(|({user_agent}[^"]+))"?,({result}\S+)""",
   ]


}
```