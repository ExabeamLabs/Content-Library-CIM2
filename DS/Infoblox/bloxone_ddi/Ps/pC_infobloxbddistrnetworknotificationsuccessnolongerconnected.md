#### Parser Content
```Java
{
Name = infoblox-bddi-str-network-notification-success-nolongerconnected
	ParserVersion = v1.0.0
  Vendor = Infoblox
  Product = BloxOne DDI
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """: Grid member at""", """is no longer connected""" ]
  Fields = [        
	  """\d\d:\d\d:\d\d\s+({host}[\w.-]+)\s+({src_ip}[a-fA-F\d.:]+?)\s+({additional_info}[^~]+?)\s*$"""
  ]


}
```