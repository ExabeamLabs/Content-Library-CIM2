#### Parser Content
```Java
{
Name = "cisco-securenwanalytics-kv-alert-trigger-success-stealthwatch-1"
  Vendor = "Cisco"
  Product = "Cisco Secure Network Analytics"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [""" Stealthwatch[""", """ name="""", """ type="""", """ id="""]
  Fields = [
    """time=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """device="?({host}[\w.-]+)""",
    """name="({alert_name}[^"]+)"""",
    """type="({alert_type}[^"]+)"""",
    """id="?({alert_id}[^"\s]+)""",
    """(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))\s+Stealthwatch\[""",
    """sourceip="?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """targetip="?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """targetport="?({dest_port}\d+)"""
    """source_hostname="?({src_host}[\w.-]+)"""
    """target_hostname="?({dest_host}[\w.-]+)"""
    """details="({additional_info}[^"]+)"""    
  ]
  ParserVersion = "v1.0.0"


}
```