#### Parser Content
```Java
{
Name = fortinet-fortinac-kv-user-modify-success-fortinac
   ParserVersion = v1.0.0
   Vendor = Fortinet
   Product = FortiNAC
   TimeFormat = ["MMM dd yyyy HH:mm:ss","MMM dd HH:mm:ss.SSS" , "yyyy-MM-dd 'time='HH:mm:ss"]
   Conditions = [ """subtype="user"""", """devname="FortiNAC""", """action="update"""" ]
   	Fields = [
        """date=({time}\d\d\d\d-\d\d-\d\d time=\d\d:\d\d:\d\d)"""
        """devname=\"*({host}[^\"]+?)\"*(\s+\w+=|\s*$)"""
        """assetid=({asset_id}\d+)\s"""
        """\sdevid="({devid}[^"]+)""""
        """userid="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
        """firstname="({first_name}[^"]+)""""
        """lastname="({last_name}[^"]+)""""
        """email="({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)"""
        """\smsg="({additional_info}[^"]+)"""
        """cat=({category}[^=]+?)(\s+\w+=|$)"""
        """\Wsubtype="*({event_subtype}[^\"]+?)\"*(\s+\w+=|\s*$)"""
        """\Wtz="?({tz}[+-]\d+)"""
        """country="({country}[^"]+?)""""
         """action="({action}[^"]+)""""
	]
  

}
```