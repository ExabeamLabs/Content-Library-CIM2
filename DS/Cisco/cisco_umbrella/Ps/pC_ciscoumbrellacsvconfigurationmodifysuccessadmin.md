#### Parser Content
```Java
{
Name = cisco-umbrella-csv-configuration-modify-success-admin
  Vendor = Cisco
  Product = Cisco Umbrella
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ParserVersion = "v1.0.0"
  Conditions = [ """destinationServiceName =CiscoUmbrella """, """dproc=Admin """ ]
  Fields = [
    """destinationServiceName =({app}[^=]+?)\s+\w+=""",
    """>\s*"[^"]*","({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)","""",
    """>\s*("[^"]*",){2}"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """>\s*("[^"]*",){3}"({full_name}[^"]+)","""",
    """>\s*("[^"]*",){4}"({object}[^"]+)","""",
    """>\s*("[^"]*",){5}"({action}[^"]+)",""",
    """>\s*("[^"]*",){6}"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?",""",
    """>\s*("[^"]*",){8}"({additional_info}[^"]+)"""",
    """email:\s*({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))(\s\w+:|$|")""",
    """id:\s*({resource_id}\d+)\s""",
    """role:\s*({role}[^:]+?)\s*\w+:"""
  ]


}
```