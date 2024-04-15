#### Parser Content
```Java
{
Name = "okta-amfa-sk4-user-password-modify-success-passwordupdate"
Conditions = [
"""core.user.config.password_update.success"""
""""published":""""
]
ParserVersion = "v1.0.0"

json-okta-auth.Fields}[
    """target(s)?"+:[^\]]+?"+type"+:"+User"+[^\]\}]+?"+(alternateId|emailAddress)"+:(null|"+(({dest_email_address}[^@",\s]+@({dest_domain}[^"]+))|({dest_user}^@",\s])+))"""
    """target(s)?"+:[^\]]+?"+type"+:"+User"+[^\]\}]+?"+(alternateId|emailAddress)"+:(null|"+(({dest_domain}[^\\\/]+)[\/\\]+)?({dest_user}[^"]+))"""

}
```