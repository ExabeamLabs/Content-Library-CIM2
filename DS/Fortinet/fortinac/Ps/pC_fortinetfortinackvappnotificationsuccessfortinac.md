#### Parser Content
```Java
{
Name = fortinet-fortinac-kv-app-notification-success-fortinac
   ParserVersion = v1.0.0
   Vendor = Fortinet
   Product = FortiNAC
   TimeFormat = ["MMM dd yyyy HH:mm:ss","MMM dd HH:mm:ss.SSS" , "yyyy-MM-dd 'time='HH:mm:ss"]
   Conditions = [ """type="event"""", """devname="FortiNAC""", """cat="EndStation"""" ]
   	Fields = [
        """date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d)"""
        """devname=\"*({host}[^\"]+?)\"*(\s+\w+=|\s*$)"""
        """\sip=\"?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
        """mac="({src_mac}[a-fA-F\d.:]+)"""
        """\smsg="({additional_info}[^"]+)"""
        """cat=({category}[^=]+?)(\s+\w+=|$)"""
        """\Wsubtype="*({event_subtype}[^\"]+?)\"*(\s+\w+=|\s*$)"""
        """\Wtz="?({tz}[+-]\d+)"""
	]
 } 

 {
  Name = fortinet-fortixdr-kv-process-close-success-fortixdr
  ParserVersion = "v1.0.0"
  Vendor = Fortinet
  Product = FortiXDR
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"FortiXDR Connect LATAM 2"""", """sub_system=""" , """type=event""" , """devid=""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
    """\Wtype=({category}[^"]+)\ssubtype"""
    """\Wsubtype="({event_category}[^"]+)""""
    """device_name=({host}[^"\s]+)"""
    """description="({description}[^"]+)""""
    """from device \[({host}[\w\-.]+)"""
  ]


}
```