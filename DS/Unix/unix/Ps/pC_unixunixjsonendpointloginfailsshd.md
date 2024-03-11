#### Parser Content
```Java
{
Name = unix-unix-json-endpoint-login-fail-sshd
  Product = Unix
  Conditions = [ """"ident":"sshd""", """nvalid user""" ]
  Fields = ${UnixParsersTemplates.unix-activity-json.Fields}[
    """(I|i)nvalid user (({domain}[^\\:]+)\\+)?({user}[\w.'\-\\$]+)""",
    """from ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\s+from\s+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
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