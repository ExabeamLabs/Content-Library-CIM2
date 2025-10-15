#### Parser Content
```Java
{
Name = zeek-z-str-app-notifiction-dpd
  Vendor = Zeek
  Product = Zeek 
  TimeFormat = "epoch_sec"
  Conditions = [ """/dpd.log""" ]
  Fields = [
      """(({time}\d{10})\.\d{6})\s+({user_uid}[^\s]+)\s+(({src_ip}({id_orig_h}(\d{1,3}\.){3}\d{1,3})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+)\s+(({id_orig_p}({src_port}\d+))?|[^\s]+)\s+(({dest_ip}({id_resp_h}(\d{1,3}\.){3}\d{1,3})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+)\s+(({id_resp_p}({dest_port}\d+?))|[^\s]+)\s+({protocol}[^\s]+)\s+({=protocol}[^\s]+)\s+({failure_reason}([^"]+)*)\s*"""
]
  ParserVersion = "v1.0.0"


}
```