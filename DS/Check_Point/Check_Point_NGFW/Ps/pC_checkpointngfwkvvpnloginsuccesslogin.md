#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-vpn-login-success-login
  ParserVersion = "v1.0.0"
  Conditions = [ """CheckPoint""", """product:"""", """action:"Log In"""", """vpn_""" ]
  Fields = ${CheckpointParsersTemplates.checkpoint-auth.Fields}[
    """action:"+({operation}[^"]+)"""
  ]
  DupFields = [ "operation->event_name" ]

checkpoint-auth = {
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "epoch_sec"
  Fields = [
    """\Wtime:"({time}\d+)""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """\Wuser:"({user}[^"\s]+)"""",
    """\Wuser:"({last_name}[^,]+),\s*({first_name}[\w\s]+\S)\s*\(({user}.+?)\)""",
    """\Wuser:"({full_name}[^,:\("]+)\s\(({user}[^\)]+)\)""",
    """\Wsrc:"({src_ip}[A-Fa-f:\d.]+)""",
    """\Wendpoint_ip:"({dest_ip}[A-Fa-f:\d.]+)""",
    """host_ip:"({dest_ip}[^"]+)""",
    """\Wauth_method:"({auth_method}[^"]+)""",
    """\Wauth_status:"({result}[^"]+)""",
    """\sstatus:"({result}[^"]+)""",
    """\Wdomain_name:"({domain}[^"]+)""",
    """\Worigin:"({origin_ip}[^"]+)""",
    """\Worigin_sic_name:"CN=({origin_name}[^",]+)""",
    """\Wproduct:"({product_name}[^"]+)""",
    """reason:"({failure_reason}[^"]+)""",
    """\Wsrc_machine_name:"({src_host}[\w\-.]+)""",
    """\Wifdir:"({direction}[^"]+)""",
  
}
```