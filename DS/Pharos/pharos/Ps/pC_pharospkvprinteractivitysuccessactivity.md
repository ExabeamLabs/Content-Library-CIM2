#### Parser Content
```Java
{
Name = "pharos-p-kv-printer-activity-success-activity"
Vendor = "Pharos"
Product = "Pharos"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
""" JobName ="""
""" UserName ="""
""" DeviceName ="""
""" Time_Printed="""
]
Fields = [
"""\sUserName =({user}.+?)(\s+\w+=|\s*$)"""
"""\sJobName ="?({object}.+?)"?(\s+\w+=|\s*$)"""
"""\sPages=({num_pages}\d+)(\s+\w+=|\s*$)"""
"""\sFileSize=({bytes}\d+)(\s+\w+=|\s*$)"""
"""\sDeviceName =({printer_name}.+?)(\s+\w+=|\s*$)"""
"""\sDeviceName =({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))(\s+\w+=|\s*$)"""
"""\sApplicationName =(Unknown|({process_name}.+?))(\s+\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```