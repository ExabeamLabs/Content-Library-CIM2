#### Parser Content
```Java
{
Name = pan-gp-csv-vpn-logout-success-logout-2
  ParserVersion = v1.0.0
  Conditions = [
""",GLOBALPROTECT,""",
""",logout,"""
  ]

raw-pan-vpn-event  = {
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy/MM/dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Fields = [
    """,GLOBALPROTECT,([^,]+,){2}({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z),""",
    """({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d)""",
    """:\d\d:\d\d\s+({host}[\w.-]+)\s""",
    """\d\d:\d\d:\d\d\s({host}[^,]+?)\s*\d*,({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d),""",
    """({vpn_client}GLOBALPROTECT),"+(({domain}[^\\,]+)\\)?(-|na|({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"+,""",
    """({vpn_client}GLOBALPROTECT),(?:[^,]*,){4}({event_name}[^,]+)?,({operation}[^,]*)(?:[^,]*,){3}((({domain}[^\\,]+)\\)?(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|(pre-logon|\.{3}|(-|na|({src_user}({user}[\w\.\-]{1,40}\$?))))))?,({country}[^,]+)?,[^,]*,(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?),[^,]*,(|0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),""",
    #""",GLOBALPROTECT,([^,]*,){19}"({os}[^"]+)"""",
    """,GLOBALPROTECT,([^,]*,){18}(|(?i)any|({os}[^,]*)),"""
    """,GLOBALPROTECT,([^,]*,){19}("+,|"+[^"]+"+,)([^,]*,){3}("+,|"+({additional_info}[^"]+)"+,)""",
    """,(|\s*({failure_reason}[^,]+?)\s*"*\s*),(""+|"({additional_info}[^"]+)"),({result}failure)""",
    """,GLOBALPROTECT,([^,]*,){19}("+,|"+[^"]+"+,)([^,]*,){3}("+,|"+[^"]+"+,)({result}failure|success)""",
    """,GLOBALPROTECT,([^,]*,){15}({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})""",
    """,GLOBALPROTECT,([^,]*,){19}"*(|({device_type}[^=]+?))"*\s*,""",
    """,GLOBALPROTECT,([^,]*,){10}({src_host}[\w\-\.]+)""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))""",
    """,(success|failure),[^,]*?,({session_duration}\d+),"""
    """,GLOBALPROTECT,([^,]*,){6}(|({auth_type}[^,]*)),""",
    """,({serial_num}\d+),GLOBALPROTECT,"""
    """,GLOBALPROTECT,([^,]*,){44}({device_name}({host}[^,]+)),"""
  
}
```