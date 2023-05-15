#### Parser Content
```Java
{
Name = checkpoint-ngfw-str-app-logout-success-loggedout
  ParserVersion = "v1.0.0"
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """]: """ , """][""", """ logged out """ ]
  Fields = [
    """\[({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\[[^\]]*\]\[[^\]]*\]\[[^\]]*\]\s*<\d+>(({src_host}[\w\-.]+)\s+)?({process_name}.+?)\[({process_id}\d+)\]:\s*({additional_info}User\s+({user}[^\s]+)\s+logged out.*?)\s*$""",
  ]


}
```