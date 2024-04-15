#### Parser Content
```Java
{
Name = "cisco-ise-kv-app-logout-accounting"
  Vendor = "Cisco"
  Product = "Cisco ISE"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """CISE_TACACS_Accounting"""
    """Tacacs-Accounting:"""
    """TACACS+ Accounting STOP"""
    """Authen-Method=TacacsPlus"""
  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\.\d+"""
    """({host}[^\s]+)\sCISE_TACACS_Accounting"""
    """Device IP Address=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,"""
    """Remote-Address=(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),"""
    """({operation}Accounting STOP)"""
    """Privilege-Level=({privileges}[^,]+),"""
    """({app}TACACS\+ Accounting)"""
    """\sUser=(({email_address}[^\s]+?@[^\s]+?)|({user}[^,]+)),"""
  ]
  ParserVersion = "v1.0.0"


}
```