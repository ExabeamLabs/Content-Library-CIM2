#### Parser Content
```Java
{
Name = unix-unix-json-endpoint-login-fail-sshd
  Product = Unix
  Conditions = [ """"ident":"sshd""", """nvalid user""" ]
  Fields = ${UnixParsersTemplates.unix-activity-json.Fields}[
    """(I|i)nvalid user (({domain}[^\\:]+)\\+)?({user}[\w.'\-\\$]+)""",
    """from ({src_ip}[a-fA-F\d.:]+)""",
    """\s+from\s+(::[\w]+:)?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
  ]
  ParserVersion = "v1.0.0"

unix-activity-json = {
    Vendor = Unix
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Fields = [
      """"host(name)?":"({host}[^"]+)""",
      """"ident":"({event_code}[^"]+)""",
      """"pid":"({process_id}\d+)""",
      """"time(stamp)?":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ?)""",
    
}
```