#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-alert-trigger-monitor
  ParserVersion = "v1.0.0"
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """logger:""", """product:""", """ monitor """ ]
  Fields = [
    """logger:\s*\d\d:\d\d:\d\d\s*({action}\w+)\s*({host}[\w.\-]+)""",
    """product:\s*({product_name}.+?);""",
    """\Wsrc:\s*(|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?);""",
    """\Ws_port:\s*(|({src_port}\d+));""",
    """\Wdst:\s*(|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?);""",
    """\Wservice:\s*(|({dest_port}\d+));""",
    """\Wproto:\s*(|({protocol}.+?));""",
    """\Wrule:\s*(|({rule}.+?));""",
    """\Wrule_name:\s*(|({rule}.+?));""",
    """\Wuser:\s*(|({user}.+?));""",
    """\Wuser:\s*({full_name}.+?)\s*\(({account}.+?)\)""",
    """\Wsrc_machine_name:\s*({email_address}[^;]+@[^;]+?);""",
    """\Wxlatesrc:\s*(|({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}));""",
    """\Wxlatesport:\s*(|({src_translated_port}\d+));""",
    """\Wxlatedst:\s*(|({dest_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}));""",
    """\Wxlatedport:\s*(|({dest_translated_port}\d+));""",
    """\Wservice_id:\s*(|({protocol}.+?));""",
  ]
   DupFields = [ "action->event_name" ]


}
```