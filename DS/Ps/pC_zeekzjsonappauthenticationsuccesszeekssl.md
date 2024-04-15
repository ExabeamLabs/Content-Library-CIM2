#### Parser Content
```Java
{
Name = "zeek-z-json-app-authentication-success-zeekssl"
Conditions = [ """ zeek_ssl """, """"id.orig_h""", """"id.resp_h""" ]
ParserVersion = "v1.0.0"

json-bro-activity.Fields}[
    """"helo":\s*"({helo}[^"]+)""",
    """"mailfrom":\s*"({src_email_address}[^"@]+@({exter_domain_sender}[^"@]+))"""
    """rcptto":\[({email_recipients}"({dest_email_address}[^",@]+@({exter_domain_recipient}[^"@,]+))".*?)\]""",
    """"subject":\s*"({email_subject}[^"]+)""",
    """"user_agent":\s*"({user_agent}[^"]+)"""
  
}
```