#### Parser Content
```Java
{
Name = "sophos-xgfirewall-kv-vpn-login-logout-sfw"
Vendor = "Sophos"
Product = "Sophos XG Firewall"
TimeFormat = "yyyy-MM-dd' time='HH:mm:ss"
Conditions = [
"""device="SFW""""
"""log_component="SSL VPN"""
]
Fields = [
"""\Wdevice_name="({host}[^"]+)"""
"""\Wdate=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d)"""
"""\Wstatus="({result}[^"]+)"""
"""\Wpriority=(|({alert_severity}.+?))(\s+\w+=|\s*$)"""
"""\Wsrc_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdst_ip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Wprotocol="({protocol}[^"]+)"""
"""\Wsrc_port=({src_port}\d+)"""
"""\Wdst_port=({dest_port}\d+)"""
"""\Wlog_component="({operation}[^"]+)""""
"""\Wuser_name="({user}[\w\.\-]{1,40}\$?)""""
"""\Wuser_name="({email_address}[^\s@"]+@[^\s@"]+)""""
"""\Wfw_rule_id=({rule}\d+)"""
"""\Win_interface=(({src_interface}\d+)|"({=src_interface}[^"]+?)")"""
"""\Wout_interface=(({dest_interface}\d+)|"({=dest_interface}[^"]+?)")"""
"""\Wreason=({failure_reason}.+?)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```