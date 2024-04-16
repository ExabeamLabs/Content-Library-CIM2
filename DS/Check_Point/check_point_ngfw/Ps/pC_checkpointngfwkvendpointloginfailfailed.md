#### Parser Content
```Java
{
Name = "checkpoint-ngfw-kv-endpoint-login-fail-failed"
Conditions = [
  """CheckPoint"""
  """product:""""
  """action:"Failed Log In""""
]
ParserVersion = "v1.0.0"
Vendor = "Check Point"
Product = "Check Point NGFW"
TimeFormat = "epoch_sec"
Fields = [
  """\Wtime(:|=)"({time}\d{10})"""
  """\W({host}[\w\-.]+) CheckPoint"""
  """\Wuser:"(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-]{1,40}\$?)))""""
  """\Wuser:"({last_name}[^,]+),\s*({first_name}[\w\s]+\S)\s*\(({user}[\w\.\-]{1,40}\$?)\)"""
  """\Wuser:"({full_name}[^,:\("]+)\s\(({user}[\w\.\-]{1,40}\$?)\)"""
  """\Wsrc:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wendpoint_ip:"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """host_ip:"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wauth_method:"({auth_method}[^"]+)"""
  """\Wauth_status:"({result}[^"]+)"""
  """\sstatus:"({result}[^"]+)"""
  """\WDomain:\s+({domain}[^";]+)"""
  """\Wdomain_name:"({domain}[^"]+)"""
  """\Worigin:"({origin_ip}[^"]+)"""
  """\Worigin_sic_name:"CN=({origin_name}[^",]+)"""
  """\Wproduct:"({product_name}[^"]+)"""
  """reason:"({failure_reason}[^"]+?)\s*""""
  """\Wsrc_machine_name:"({src_host}[\w\-.]+)"""
  """\Wifdir:"({direction}[^"]+)"""
  """description:"({failure_reason}({additional_info}[^";]+))""""
]


}
```