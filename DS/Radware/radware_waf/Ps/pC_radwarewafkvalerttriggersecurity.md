#### Parser Content
```Java
{
Name = radware-waf-kv-alert-trigger-security
  Vendor = Radware
  Product = Radware WAF
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """ServerName =""", """Type=Security""", """WebUser=""", """Attackname=""", """Threatcategory=""", """Tunnel=""" ]
  Fields = [
     """ServerName ="+({host}[^\s]+)""",
     """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
     """Description="+\s*({additional_info}[^"]+?)\s*"""",
     """Title="+({alert_name}[^"]+)""",
     """\sPriority=({alert_severity}[^\s]+)""",
     """\sAttackname="+({alert_type}[^"]+)""",
     """\sSourceIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """\sSourcePort=({src_port}\d+)""",
     """\sURI="+\s*({uri_path}[^"]+)""",
     """WebApp="+({app}[^"]+)""",
     """WebUser="+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  ]
  ParserVersion = "v1.0.0"


}
```