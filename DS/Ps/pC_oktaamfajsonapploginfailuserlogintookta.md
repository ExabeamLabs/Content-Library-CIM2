#### Parser Content
```Java
{
Name = "okta-amfa-json-app-login-fail-userlogintookta"
Conditions = [ """"displayMessage": "User login to Okta"""", """"legacyEventType": "core.user_auth.login_failed"""" ]
ParserVersion = "v1.0.0"

json-okta-auth.Fields}[
    """target(s)?"+:[^\]]+?"+type"+:"+User"+[^\]\}]+?"+(alternateId|emailAddress)"+:(null|"+(({dest_email_address}[^@",\s]+@({dest_domain}[^"]+))|({dest_user}^@",\s])+))"""
    """target(s)?"+:[^\]]+?"+type"+:"+User"+[^\]\}]+?"+(alternateId|emailAddress)"+:(null|"+(({dest_domain}[^\\\/]+)[\/\\]+)?({dest_user}[^"]+))"""

}
```