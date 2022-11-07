#### Parser Content
```Java
{
Name = ca-pamsc-csv-endpoint-login-fail-baduserid
  ParserVersion = v1.0.0
  Conditions = [ """Transaction: login""", """PAM-CMN-0900:""", """gkpsyslog""" ]
  Fields = ${PamParsersTemplates.pam-authentication.Fields}[
    """({event_name}Bad User ID)""",
  ]
  DupFields = [ "event_name->failure_reason" ]

pam-authentication = {
    Vendor = CA Technologies
    Product = CA Privileged Access Manager Server Control
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """\screated\s*=\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """\sUser\s*:\s*CN=({full_name}[^,]+),\s*({user_ou}.+?),\s*Transaction:""",
      """\sUser\s*:\s*({email_address}[^,@]+@[^,]+)""",
      """\sUser\s*:\s*(?:unknown|({user}[^@=,]+)),\s*Transaction:""",
      """\sUser Group\s*:\s*CN=({group_name}[^,]+),\s*({group_ou}.+?),\s*Port:""",
      """\sNat\/Proxy IP\s*:\s*({src_ip}[a-fA-F\d.:]+)""",
      """\sDetails:[^;]*:\s+({event_name}[^;]+?)\s*(;|$)""",
      """\sPrivate IP\s*:\s*({src_ip}[a-fA-F\d.:]+)""",
      """\sSource IP\s*:\s*({src_ip}[a-fA-F\d.:]+)""",
      """(?i)\sDevice Name\s*:\s*(?:\- \-|({dest_host}[^,]+))""",
      """\sPort\s*:\s*({dest_port}\d+)""",
      """\sAccess/Protocol\s*:\s*(?:\- \-|({protocol}[^,]+))""",
      """\sService/App\s*:\s*(?:\- \-|({app}[^,]+))""",
    ]
    DupFields = [ "dest_host->host" 
}
```