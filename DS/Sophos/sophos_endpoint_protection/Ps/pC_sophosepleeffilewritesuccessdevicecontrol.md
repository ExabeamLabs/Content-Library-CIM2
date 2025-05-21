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
          """usrName =[^\\]*\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)""",
          """src=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
          """domain=({domain}.+?)\s+(\w+=|$)""",
          """DeviceID=(?:\s|({device_id}.+?))\s+(\w+=|$)""",
          """Model=(?:\s|({device_type}.+?))\s+(\w+=|$)"""
  ]
  ParserVersion = "v1.0.0"


}
```