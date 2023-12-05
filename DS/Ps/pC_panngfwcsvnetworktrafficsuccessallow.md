#### Parser Content
```Java
{
Name = pan-ngfw-csv-network-traffic-success-allow
Conditions = [
  """,TRAFFIC,"""
  """,allow,"""
  """APC-PANORAMA-LOGS"""
]
ParserVersion = "v1.0.0"

cef-palo-alto-networks-firewall.Fields}[
     """\sreason=(?:n\/a|({failure_reason}.+?))\s+(\w+=|$)"""
 
}
```