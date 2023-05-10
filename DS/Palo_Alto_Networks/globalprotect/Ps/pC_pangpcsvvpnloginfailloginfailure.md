#### Parser Content
```Java
{
Name = pan-gp-csv-vpn-login-fail-loginfailure
  ParserVersion = v1.0.0
  Conditions = [
""",GLOBALPROTECT,""",
""",login,""",
""",failure,"""
  ]

raw-pan-vpn-event  = {
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Fields = [
    """,GLOBALPROTECT,([^,]+,){2}({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),""",
    """({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)""",
    """:\d\d:\d\d\s+({host}[\w.-]+)\s""",
    """\d\d:\d\d:\d\d\s({host}[^,]+?)\s*\d*,({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d),""",
    """({vpn_client}GLOBALPROTECT),"+((({domain}[^\\,]+)\\)?(({email_address}[^@,]+@[^@,]+)|({user}[^,]+)))"+,""",
    """({vpn_client}GLOBALPROTECT),(?:[^,]*,){4}({event_name}[^,]+)?,({operation}[^,]*)(?:[^,]*,){3}((({domain}[^\\,]+)\\)?((({user}[^@,]+)@({=domain}[^@,.]+\.lan))|({email_address}[^@,]+@[^@,]+)|(pre-logon|\.{3}|({=user}[^,]+))))?,({country}[^,]+)?,[^,]*,(|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),[^,]*,(|0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),""",
    """GLOBALPROTECT,([^,]*,){19}"({os}[^"]+)"""",
    """GLOBALPROTECT,([^,]*,){19}("+,|"+[^"]+"+,)([^,]*,){3}("+,|"+({additional_info}[^"]+)"+,)""",
    """,(|\s*({failure_reason}[^,]+?)\s*"*\s*),(""+|"({additional_info}[^"]+)"),({result}failure)""",
    """GLOBALPROTECT,([^,]*,){19}("+,|"+[^"]+"+,)([^,]*,){3}("+,|"+[^"]+"+,)({result}failure|success)""",
    """GLOBALPROTECT,([^,]*,){15}({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})""",
    """GLOBALPROTECT,([^,]*,){19}"*(|({device_type}[^=]+?))"*\s*,""",
    """GLOBALPROTECT,([^,]*,){10}({src_host}[^,]+)"""
  
}
```