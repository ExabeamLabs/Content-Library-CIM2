#### Parser Content
```Java
{
Name = "cisco-ise-cef-endpoint-login-success-adlogin"
Vendor = "Cisco"
Product = "Cisco ISE"
TimeFormat = "epoch"
Conditions = [
"""|TACACS+ Accounting"""
"""cat=Tacacs-Accounting"""
"""ad.Service=Login"""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""ad.NetworkDeviceName =({dest_host}[^\s]+)"""
"""CmdAV\\=({command}.+?)\s\]"""
"""ad.User=({user}[^\s]+)"""
"""ad.Device_,IP_,Address=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""({app}TACACS)"""
"""ad.Privilege-Level=({privileges}\d+)"""
"""ad.Remote-Address=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
ParserVersion = "v1.0.0"


}
```