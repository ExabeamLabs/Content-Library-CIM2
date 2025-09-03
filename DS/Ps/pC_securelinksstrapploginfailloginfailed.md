#### Parser Content
```Java
{
Name = "securelink-s-str-app-login-fail-loginfailed"
  Conditions = [
    """ Login failed:"""
    """SecureLink"""
    """ User:"""
  ]
  ParserVersion = "v1.0.0"

mimecast-json-event.Fields}[
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z) [\w.\-]+ """,
    """IP:\s({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}),""",
    """"user":"(|({email_address}[^@]+@[^"]+?))"""",
    """\sReason:\s(|({failure_reason}[^=]+?))(\s+\w+=|\s*$)""",
    """\sApplication:\s*({app}[^,]+?),""",
    """"user":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  
}
```