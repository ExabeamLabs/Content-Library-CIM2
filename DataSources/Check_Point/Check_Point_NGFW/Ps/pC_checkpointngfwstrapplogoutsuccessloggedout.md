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
    """\[({src_ip}[A-Fa-f:\d.]+)\]\[[^\]]*\]\[[^\]]*\]\[[^\]]*\]\s*<\d+>(({src_host}[\w\-.]+)\s+)?({process_name}.+?)\[({process_id}\d+)\]:\s*({additional_info}User\s+({user}[^\s]+)\s+logged out.*?)\s*$""",
  ]


}
```