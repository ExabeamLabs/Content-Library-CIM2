#### Parser Content
```Java
{
Name = netskope-casb-sk4-app-activity-success-webmail
  Vendor = Netskope
  Product = Netskope CASB 
  TimeFormat = "epoch_sec"
  ParserVersion = v1.0.0
  Conditions = [ """"organization_unit":"""" ,""""access_method":"""",""""aggregated_user":"""",""""app_session_id":""",""""appcategory":"Webmail""""]
  Fields = [
    """"timestamp":({time}\d{10})""",
    """requestClientApplication=({app}.+?)\s+(\w+=|$)""", 
    """"category":"({additional_info}[^"]+)""",
    """"user":"(unknown|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))""",
    """"access_method":\s*"({auth_method}[^\"]+)""",
    """"app":\s*"\[?({app}[^\"\]]+)""",
    """"_id":"({alert_id}[^",]+)""",
    """"policy":"({alert_name}[^",]+)"""
    """"browser":"((U|u)nknown|({browser}[^"]+))""",
    """"dstport":({dest_port}\d+)""",
    """"numbytes":({bytes}\d+)""",
    """"src_country":"({src_country}[^="]+)""",
    """"dstip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"srcip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]


}
```