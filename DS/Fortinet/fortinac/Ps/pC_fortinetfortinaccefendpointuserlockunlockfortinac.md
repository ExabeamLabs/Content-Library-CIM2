#### Parser Content
```Java
{
Name = fortinet-fortinac-cef-endpoint-user-lock-unlock-fortinac
   ParserVersion = v1.0.0
   Vendor = Fortinet
   Product = FortiNAC
   TimeFormat = ["MMM dd yyyy HH:mm:ss","MMM dd HH:mm:ss.SSS"]
   Conditions = [ """CEF:""", """|Fortinet|FortiNAC-""", """cat=user""" ]
   Fields = [
    """\Wrt=({time}\w{1,3}\s\d\d\s\d\d:\d\d:\d\d.\d\d\d)"""
    """cat=({category}[^=]+?)(\s+\w+=|$)"""
    """CEF:([^\|]*\|){5}({event_name}[^\|]+)"""
    """\smsg=({additional_info}[^"]+)""""
    """\smsg=User\s({full_name}[^"\s@]+\s+[^"\s@]+)\s"""
    """host\s({host}[\w\-.]+)"""
   ]
 

}
```