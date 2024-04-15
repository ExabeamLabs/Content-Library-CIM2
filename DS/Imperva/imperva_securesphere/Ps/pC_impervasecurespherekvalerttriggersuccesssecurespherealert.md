#### Parser Content
```Java
{
Name = "imperva-securesphere-kv-alert-trigger-success-securespherealert"
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """|at=Securesphere Alert|"""
  """|g="""
  """|u="""
]
Fields = [
  """\|ad=({alert_name}.+?)( (from|by|in) .+?)?\|"""
  """\|an=({alert_type}[^|]+)"""
  """\|s=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\|d=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\|u=(?:n\/a|({user}[^|]+))"""
  """\|g=({process_name}.+?)\s*\|"""
]
ParserVersion = "v1.0.0"


}
```