#### Parser Content
```Java
{
Name = sophos-ep-leef-file-write-success-devicecontrol
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"	
  Conditions = [ """LEEF:1.0|Sophos|Enterprise Console|""","""|Device control - Alert only|""" ]
  Fields = [
          """devTime=({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})""",
          """ComputerName =({dest_host}.+?)\s+(\w+=|$)""",
          """LEEF:[^|]*\|Sophos\|Enterprise Console\|[^|]*\|({operation}[^|]*)\|""",
          """usrName =[^\\]*\\({user}.+?)\s+(\w+=|$)""",
          """src=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
          """domain=({domain}.+?)\s+(\w+=|$)""",
          """DeviceID=(?:\s|({device_id}.+?))\s+(\w+=|$)""",
          """Model=(?:\s|({device_type}.+?))\s+(\w+=|$)"""
  ]
  ParserVersion = "v1.0.0"


}
```