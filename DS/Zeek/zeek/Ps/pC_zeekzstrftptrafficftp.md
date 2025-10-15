#### Parser Content
```Java
{
Name = zeek-z-str-ftp-traffic-ftp
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """/ftp.log""" ]
  Fields = [
# DL fields are removed
    """({time}\d{10})\.\d{6}\s+({user_uid}[^\s]+)\s+(({src_ip}({id_orig_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?)))|[^\s]+)\s+(({id_orig_p}({src_port}\d+?))|[^\s]+)\s+(({dest_ip}({id_resp_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?)))|[^\s]+)\s+(({id_resp_p}({dest_port}\d+?))|[^\s]+)\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+({password}[^\s]+)\s+({command}[^\s]+)\s+({arg}[^\s]+)\s+([^\s]+)\s+({bytes}\d+)\s+([^\s]+)\s+([^\s]+)\s+([^\s]+)\s+([^\s]+)\s+([^\s]+)\s+([^\s]+)\s+([^\s]+?)\s*"""
    """\d{10}\.\d{6}\s([^\s]+\s){8}(?:-|({object}[^\s]+))\s+(?:-|({mime}[^\s]+))\s+(?:-|({bytes}\d+))\s*"""
	]
  ParserVersion = "v1.0.0"


}
```