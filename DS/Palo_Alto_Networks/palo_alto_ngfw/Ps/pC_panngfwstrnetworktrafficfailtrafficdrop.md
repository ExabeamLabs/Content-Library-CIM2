#### Parser Content
```Java
{
Name = "pan-ngfw-str-network-traffic-fail-trafficdrop"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
Conditions = [  """,Deny,""", """ TRAFFIC drop """ ]
Fields = [
  """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[A-Fa-f:\d.]+)\s+\d+\s+({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+)\s+\S+\s+({event_category}TRAFFIC)\s+({subtype}\S+)\s+\S+\s+\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(0.0.0.0|({src_ip}(?!::)[a-fA-F\d.:]+))\s+(0.0.0.0|({dest_ip}(?!::)[a-fA-F\d.:]+))\s+(0.0.0.0|({src_translated_ip}(?!::)[a-fA-F\d.:]+))\s+(0.0.0.0|({dest_translated_ip}(?!::)[a-fA-F\d.:]+))\s+({rule}[^\s]*?)\s+.*?\s+({src_network_zone}\S+)\s+\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+\S+\s+\d+\s+(0|({src_port}\d+))\s+(0|({dest_port}\d+))\s+(0|({src_translated_port}\d+))\s+(0|({dest_translated_port}\d+))\s+\S+\s+({protocol}\S+)\s+({action}\S+)\s+({bytes}\d+)\s+({bytes_out}\d+)\s+({bytes_in}\d+)\s+\d+\s+\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+\d+\s+({category}\S+)\s+""",
  """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
]
ParserVersion = "v1.0.0"


}
```