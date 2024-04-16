#### Parser Content
```Java
{
Name = "okta-amfa-json-app-login-fail-authenticateuserviainbounddelauth"
Conditions = [ """"displayMessage": "Authenticate user via inbound delauth"""", """"result": "FAILURE"""" ]
ParserVersion = "v1.0.0"

json-okta-auth.Fields}[
    """target(s)?"+:[^\]]+?"+type"+:"+User"+[^\]\}]+?"+(alternateId|emailAddress)"+:(null|"+(({dest_domain}[^\\\/]+)[\/\\]+)?(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-]{1,40}\$?)+))""""

}
```