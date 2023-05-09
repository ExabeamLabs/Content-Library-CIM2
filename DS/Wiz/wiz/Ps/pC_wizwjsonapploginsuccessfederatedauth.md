#### Parser Content
```Java
{
Name = wiz-w-json-app-login-success-federatedauth
 ParserVersion = v1.0.0
 Vendor = Wiz
 Product = Wiz
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
 Conditions = [ """,Login,""", """"name": "federated-authenticate"""", """"name": "login"""", """,SUCCESS""" ]
 Fields = [
   """ACCOUNT,({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,6}Z)""",
   """({event_name}Login)""",
   """"user_name":\s*"(({email_address}[^@]+@[^\s"]+?)|({user}[^\s]+?))"""",
   """\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.[^,]+,({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,"?(|({user_agent}[^"]+))"?,({result}\S+)""",
   ]


}
```