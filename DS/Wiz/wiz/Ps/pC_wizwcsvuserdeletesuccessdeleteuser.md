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
   """DeleteUser,[^}]+?"id"+:[^}]+\|({dest_email_address}[^@]+@[^\s"]+?)"+\}""",
   """,({email_address}[^@\s\|]+@[^\s"]+?),USER_ACCOUNT""",
   """\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.[^,]+,({src_ip}[a-fA-F\d.:]+?),"?(|({user_agent}[^"]+))"?,({result}\S+)""",
   ]


}
```