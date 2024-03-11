#### Parser Content
```Java
{
Name = pan-tesm-csv-alert-trigger-hipmatch
  Vendor = Palo Alto Networks
  Product = GlobalProtect 
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """,HIPMATCH,""" ]
  Fields = [ 
        """\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d ({host}\S+)"""
        """,({serial_num}\d+),({event_name}HIPMATCH),\d+,\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),(({domain}[^,\\]+)\\+)?({user}[^\\\s,]+),({virtual_system}[^,]+),({src_host}[^,]+),({os}[^,]+),({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({hip_profile_name}[^,]+),({repeat_count}[^,]+),({hip_type}[^,]+),([^,]*,){2}({seq_num}\d+),({action_flags}[^,]+),([^,]*,){5}({firewall}[^,]+)"""
  ]
  ParserVersion = v1.0.0


}
```