#### Parser Content
```Java
{
Name = "checkpoint-ngfw-kv-network-traffic-scans"
 Vendor = "Check Point"
 Product = "Check Point NGFW"
 TimeFormat = "epoch_sec"
 Conditions = [ """cu_rule_category""", """:"Scans"""" ]
Fields = [
    """(\"\s|,)"?time"?:"?({time}\d{10})""",
    """\Waction"?:"({action}[^",;]+)""",
	  """\Wifdir"?:"({direction}\w+[^"])""",
    """\Worigin"?:"({origin_ip}[A-Fa-f:\d.]+)""",
    """\Worigin_?sic_?name"?:"CN=({origin_name}[^",]+)""",
    """\Wsrc"?:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wxlatesrc"?:"({src_translated_ip}[A-Fa-f:\d.]+)""",
    """\Wxlatedst"?:(0\.0\.0\.0|({dest_translated_ip}[A-Fa-f:\d.]+))""",
    """\Wxlatesport"?:"?({src_translated_port}\d+)""",
    """\Wxlatedport"?:"?({dest_translated_port}\d+)""",
    """\Wsrc_machine_name"?:"({src_host}[^"]+)""",
    """\Wsrc_machine_name"?:"({src_host}[^"@]+)@({domain}[^"]+)""",
    """\Wdst_machine_name"?:"({dest_host}[^"]+)""",
    """\Wdst_machine_name"?:"({dest_host}[^"@]+)@({domain}[^"]+)""",
    """\W(user|src_user_name|dst_user_name)"?:"({full_name}[^\"\(]+?)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """\W(user|src_user_name|dst_user_name)"?:"({full_name}[^,:\("]+)\s\((({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|)(+]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)""",
    """cu_rule_category"?:"({rule_type}[^"]+)""",
    """cu_rule_id"?:"({rule_id}[^"]+)""",
    """\Wevent_name"?:"({event_name}[^",]+)""",
    """\Wproto"?:"?({protocol}[^"]+)""",
    """\Wservice"?:"?({dest_port}\d+)""",
    """\Wseverity"?:"?({severity}[^"]+)"""
]
  ParserVersion = "v1.0.0"


}
```