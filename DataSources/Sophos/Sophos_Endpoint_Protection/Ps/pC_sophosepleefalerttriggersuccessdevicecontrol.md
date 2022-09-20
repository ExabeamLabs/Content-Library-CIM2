#### Parser Content
```Java
{
Name = sophos-ep-leef-alert-trigger-success-devicecontrol
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"	
  Conditions = [ """LEEF:1.0|Sophos|Enterprise Console|""","""|Device control - Blocked|""" ]
  Fields = [
          """EventID=({alert_id}[\d]+)""",
          """devTime=({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})""",
          """LEEF:[^|]*\|Sophos\|Enterprise Console\|[^|]*\|({alert_name}[^|]*)\|""",
          """Model=({alert_type}.+?)\s+(\w+=|$)""",
          """usrName =[^\\]*\\({user}.+?)\s+(\w+=|$)""",
          """ComputerName =({dest_host}.+?)\s+(\w+=|$)""",
          """src=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
          """domain=({domain}.+?)\s+(\w+=|$)""",
          """DeviceID=(?:\s|({device_id}.+?))\s+(\w+=|$)""",
          """ActionName =({action}.+?)\s+(?:\w+=|$)"""
  ]
  ParserVersion = "v1.0.0"


}
```