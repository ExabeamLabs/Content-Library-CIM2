#### Parser Content
```Java
{
Name = fortinet-fortinac-cef-app-notification-success-fortinac
   ParserVersion = v1.0.0
   Vendor = Fortinet
   Product = FortiNAC
   TimeFormat = ["MMM dd yyyy HH:mm:ss","MMM dd HH:mm:ss.SSS"]
   Conditions = [ """CEF:""", """|Fortinet|FortiNAC-""", """cat=EndStation""" ]
   Fields = [
    """\Wrt=({time}\w{1,3}\s\d\d\s\d\d:\d\d:\d\d.\d\d\d)"""
    """cat=({category}[^=]+?)(\s+\w+=|$)"""
    """CEF:([^\|]*\|){5}({event_name}[^\|]+)"""
    """\smsg=({additional_info}[^"]+)""""
   """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
   """\ssmac=({src_mac}[a-fA-F\d.:]+)"""
   """\Wshost=({host}[\w\-.]+)"""
   """suid=({user_sid}[^\s]+)"""
   ]
 

}
```