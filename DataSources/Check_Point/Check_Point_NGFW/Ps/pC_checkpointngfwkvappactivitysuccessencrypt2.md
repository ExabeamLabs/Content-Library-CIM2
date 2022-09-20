#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-app-activity-success-encrypt-2
  ParserVersion = "v1.0.0"
  Product = Check Point NGFW
  Conditions = [ """product:""", """VPN-1 & FireWall-1;""", """ encrypt """ ]

raw-checkpoint-firewall = {
  Vendor = Check Point
  TimeFormat = "epoch_sec"
  Fields = [
    """\s({host}[\w\-\.]+)\s+product:\s*VPN-1 & FireWall-1;""",
    """\s({action}\w+)\s+\S+\s+product:\s*VPN-1 & FireWall-1;""",
    """logger:\s*\d\d:\d\d:\d\d\s*({action}\w+)\s*({host}[\w.\-]+)""",
    """({product_name}VPN-1 & FireWall-1);""",
    """\Wdate=\s*({time}\d{10})[;\]]""",
    """\Wsrc:\s*(|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}));""",
    """\Ws_port:\s*(|({src_port}\d+));""",
    """\Wdst:\s*(|({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}));""",
    """\Wservice:\s*(|({dest_port}\d+));""",
    """\Wproto:\s*(|({protocol}.+?));""",
    """\Wrule:\s*(|({rule}.+?));""",
    """\Wrule_name:\s*(|({rule}.+?));""",
    """\Wuser:\s*(|({user}.+?));""",
    """\Wuser:\s*({full_name}.+?)\s*\(({account}.+?)\)""",
    """\Wsrc_machine_name:\s*({email_address}[^;]+@[^;]+?);""",
    """\Wpolicy_name=\s*(|({policy_name}.+?))[;\]]""",
    """\Wi/f_dir:\s*(|({direction}.+?));""",
    """\Wxlatesrc:\s*(|({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}));""",
    """\Wxlatesport:\s*(|({src_translated_port}\d+));""",
    """\Wxlatedst:\s*(|({dest_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}));""",
    """\Wxlatedport:\s*(|({dest_translated_port}\d+));""",
    """\Wservice_id:\s*(|({protocol}.+?));""",
  ]
   DupFields = [ "action->event_name" 
}
```