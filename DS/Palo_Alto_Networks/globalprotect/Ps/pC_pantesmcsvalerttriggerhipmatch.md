#### Parser Content
```Java
{
Name = pan-tesm-csv-alert-trigger-hipmatch
  Vendor = Palo Alto Networks
  Product = GlobalProtect 
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
  Conditions = [ """,HIPMATCH,""" ]
  Fields = [ 
    """\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d ({host}\S+)"""
    """,({serial_num}\d+),({event_name}HIPMATCH),\d+,\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|((({domain}[^,\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))),({virtual_system}[^,]+),({src_host}[^,]+),({os}[^,]+),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({profile}[^,]+),({repeat_count}[^,]+),({hip_type}[^,]+),([^,]*,){2}({seq_num}\d+),({action_flags}[^,]+),([^,]*,){5}({firewall}[^,]+)""",        
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]
  ParserVersion = v1.0.0


}
```