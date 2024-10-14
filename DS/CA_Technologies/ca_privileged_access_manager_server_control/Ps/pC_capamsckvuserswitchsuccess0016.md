#### Parser Content
```Java
{
Name = ca-pamsc-kv-user-switch-success-0016
  Conditions = [ """Transaction: xsso""", """PAM-PRX-0016:""", """, Access/Protocol:""" ]
  Fields = ${PamParsersTemplates.pam-authentication.Fields}[
    """({event_name}Executed ""sudo su -"" using transparent login)""",
  ]
  ParserVersion = "v1.0.0"

pam-authentication = {
    Vendor = CA Technologies
    Product = CA Privileged Access Manager Server Control
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """\screated\s*=\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
      """\sUser\s*:\s*CN=({full_name}[^,]+),\s*({user_ou}.+?),\s*Transaction:""",
      """\sUser\s*:\s*({email_address}[^,@]+@[^,]+)""",
      """\sUser\s*:\s*(?:unknown|({user}[\w\.\-\!\#\^\~]{1,40}\$?)),\s*Transaction:""",
      """\sUser Group\s*:\s*CN=({group_name}[^,]+),\s*({group_ou}.+?),\s*Port:""",
      """\sNat\/Proxy IP\s*:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\sDetails:[^;]*:\s+({event_name}[^;]+?)\s*(;|$)""",
      """\sPrivate IP\s*:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\sSource IP\s*:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """(?i)\sDevice Name\s*:\s*(?:\- \-|({dest_host}[^,]+))""",
      """\sPort\s*:\s*({dest_port}\d+)""",
      """\sAccess/Protocol\s*:\s*(?:\- \-|({protocol}[^,]+))""",
      """\sService/App\s*:\s*(?:\- \-|({app}[^,]+))""",
    ]
    DupFields = [ "dest_host->host" 
}
```