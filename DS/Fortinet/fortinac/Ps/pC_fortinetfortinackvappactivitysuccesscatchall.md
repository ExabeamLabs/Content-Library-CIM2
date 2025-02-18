#### Parser Content
```Java
{
Name = fortinet-fortinac-kv-app-activity-success-catchall
   ParserVersion = v1.0.0
   Vendor = Fortinet
   Product = FortiNAC
   TimeFormat = ["MMM dd yyyy HH:mm:ss","MMM dd HH:mm:ss.SSS" , "yyyy-MM-dd 'time='HH:mm:ss"]
   Conditions = [ """type="""", """devname="FortiNAC""" ,"""action=""""]
   	Fields = [
        """date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d)"""
        """devname=\"*({host}[^\"]+?)\"*(\s+\w+=|\s*$)"""
        """\sip=\"?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
        """mac="({src_mac}[a-fA-F\d.:]+)"""
        """\smsg="({additional_info}[^"]+)"""
        """cat=({category}[^=]+?)(\s+\w+=|$)"""
        """\Wsubtype="*({event_subtype}[^\"]+?)\"*(\s+\w+=|\s*$)"""
        """\Wtz="?({tz}[+-]\d+)"""
        """action="({action}[^"]+)""""
	]
 

}
```