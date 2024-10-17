#### Parser Content
```Java
{
Name = "vmware-carbonblack-sk4-file-write-success-threatindicators-3"
Vendor = "VMware"
Product = "Carbon Black CES"
TimeFormat = "epoch"
Conditions = [
"""threatIndicators"""
""""eventType":"SYSTEM_API_CALL""""
""" attempted to write """
]
Fields = [
""""eventTime":({time}\d{13})"""
""""deviceIpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""deviceName":"(({domain}[^\\\s",]+)\\+)?({src_host}[^\\\s",]+)""""
""""email":"(({domain}[^\\",]+)\\+)?(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
""""userName":"(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""({access}write)"""
""""name":"({file_path}(({file_dir}[^"]*?[\\\/]+)?({file_name}[^\\\/"]+?(\.({file_ext}[^"]+))?)))""""
]
ParserVersion = "v1.0.0"


}
```