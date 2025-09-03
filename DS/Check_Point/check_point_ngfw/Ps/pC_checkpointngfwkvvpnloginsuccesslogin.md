#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-vpn-login-success-login
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """CheckPoint""", """product:"""", """action:"Log In"""", """cvpn_""" ]
  Fields = ${CheckpointParsersTemplates.checkpoint-auth.Fields}[
    """action:"+({operation}[^"]+)""",
    """\Wtime(:|=)"({time}\d{10})""""
  ]
  DupFields = [ "operation->event_name" ]

checkpoint-auth = {
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "epoch_sec"
  Fields = [
    """\Wtime:"({time}\d+)""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """\Wuser:"(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""",
    """\Wuser:"({last_name}[^,]+),\s*({first_name}[\w\s]+\S)\s*\(({user}[\w\.\-\!\#\^\~]{1,40}\$?)\)""",
    """\Wuser:"({full_name}[^,:\("]+)\s\((({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)""",
    """\Wsrc:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wendpoint_ip:"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """host_ip:"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\Wauth_method:"({auth_method}[^"]+)""",
    """\Wauth_status:"({result}[^"]+)""",
    """\sstatus:"({result}[^"]+)""",
    """\Wdomain_name:"({domain}[^"]+)""",
    """\Worigin:"({origin_ip}[^"]+)""",
    """\Worigin_sic_name:"CN=({origin_name}[^",]+)""",
    """\Wproduct:"({product_name}[^"]+)""",
    """reason:"({failure_reason}[^"]+)""",
    """\Wsrc_machine_name:"({src_host}[\w\-.]+)""",
    """\Wos_name:"({os}[^"]+)""""
  
}
```