#### Parser Content
```Java
{
Name = cisco-asa-cef-app-activity-success-devicedirection
   Vendor = Cisco
   Product = Cisco Adaptive Security Appliance
   ParserVersion = v1.0.0
   TimeFormat = "epoch"
   Conditions = [  """CEF:""",       """|CISCO|ASA|"""    ]
   Fields = [
      """CEF:([^\|]*\|){5}({event_name}[^\|]+)\|({priority}[^\|]+)""",
      """\WeventId=({event_code}\d+)""",
      """\Wproto=(|({protocol}.+?))(\s+\w+=|\s*$)""",
      """\WcategoryOutcome=(|/({result}.+?))(\s+\w+=|\s*$)""",
      """\Wrt=({time}\d+)""",
      """\Wsrc=({src_ip}[a-fA-F\d.:]+)""",
      """\Wspt=({src_port}\d+)""",
      """\Wdst=({dest_ip}[a-fA-F\d.:]+)""",
      """\Wdpt=({dest_port}\d+)""",
      """\Wdvc=(|({host}.+?))(\s+\w+=|\s*$)""",
      """\WdeviceDirection=(|({direction}.+?))(\s+\w+=|\s*$)"""
   ]
 

}
```