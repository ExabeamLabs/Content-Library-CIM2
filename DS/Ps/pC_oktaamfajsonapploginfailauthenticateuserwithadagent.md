#### Parser Content
```Java
{
Name = "okta-amfa-json-app-login-fail-authenticateuserwithadagent"
Conditions = [ """"displayMessage": "Authenticate user with AD agent"""", """"result": "FAILURE"""" ]
ParserVersion = "v1.0.0"

json-okta-auth.Fields}[
    """target(s)?"+:[^\]]+?"+type"+:"+User"+[^\]\}]+?"+(alternateId|emailAddress)"+:(null|"+(({dest_email_address}[^@",\s]+@({dest_domain}[^"]+))|({dest_user}^@",\s])+))"""
    """target(s)?"+:[^\]]+?"+type"+:"+User"+[^\]\}]+?"+(alternateId|emailAddress)"+:(null|"+(({dest_domain}[^\\\/]+)[\/\\]+)?({dest_user}[^"]+))"""

}
```