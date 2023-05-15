#### Parser Content
```Java
{
Name = f5-asm-kv-alert-trigger-success-shareincreased
  Vendor = F5
  Product = F5 Application Security Manager
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """device_vendor="F5"""", """device_product="ASM"""", """"Traffic Share Increased"""", """dos_attack_id="""" ]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{6}(\+|-)\d{2}:\d{2})\s({host}[\w.-]+)""",
    """dos_attack_event="({event_name}[^"]+)"""",
    """dos_attack_name="({alert_name}[^"]+)"""", 
    """source_ip="((N\/A)|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""",
	  """client_ip_geo_location="(N\/A|({country}[^"]+))""""
  ]


}
```