#### Parser Content
```Java
{
Name = sophos-ep-leef-alert-trigger-success-datacontrol
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"	
  Conditions = [ """LEEF:1.0|Sophos|Enterprise Console|""","""|Data control - Alert only|""" ]
  Fields = [ """({host}[^\s]+)\s+LEEF:1.0"""
          """devTime=({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})""",
          """ComputerName =({dest_host}.+?)\s+(\w+=|$)""",
          """LEEF:[^|]*\|Sophos\|Enterprise Console\|[^|]*\|({alert_type}[^|]*)\|""",
          """ReportingName =({alert_name}.+?)\s+(\w+=|$)""",
          """EventID=({alert_id}\d+)""",
          """usrName =[^\\]*\\({user}.+?)\s+(\w+=|$)""",
          """src=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
          """domain=({domain}.+?)\s+(\w+=|$)""",
          """FileName =({file_name}.+?)\s+(\w+=|$)""",
          """FileSize=({bytes}\d+)""",
          """DestinationValue=({target}.+?)\s+(\w+=|$)""",
  ]
  ParserVersion = "v1.0.0"


}
```