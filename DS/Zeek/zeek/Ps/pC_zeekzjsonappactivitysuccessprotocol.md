#### Parser Content
```Java
{
Name = "zeek-z-json-app-activity-success-protocol"
Product = "Zeek"
Conditions = [
"""type"""
"""protocol"""
""""ftp""""
"""zeek"""
]
ExtractionType = json
ParserVersion = "v1.0.0"

json-bro-activity.Fields}[
    """"helo":\s*"({helo}[^"]+)""",
    """"mailfrom":\s*\"({user}[\w\.\-]{1,40}\$?)@({domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""""
    """rcptto":\[({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))".*?)\]""",
    """"subject":\s*"({email_subject}[^"]+)""",
    """"user_agent":\s*"({user_agent}[^"]+)""",
    """exa_json_path=$.helo,exa_field_name=helo""",
    """exa_json_path=$.mailfrom,exa_regex=({user}[\w\.\-]{1,40}\$?)@({domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
    """exa_json_path=$.rcptto[:1],exa_regex=({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))".*?)""",
    """exa_regex=rcptto":\[({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))".*?)\]""",
    """exa_json_path=$.subject,exa_field_name=email_subject""",
    """exa_json_path=$.user_agent,exa_field_name=user_agent"""
  
}
```