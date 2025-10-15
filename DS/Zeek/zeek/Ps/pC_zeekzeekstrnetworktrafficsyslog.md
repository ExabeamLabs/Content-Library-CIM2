#### Parser Content
```Java
{
Name = "zeek-zeek-str-network-traffic-syslog"
  Vendor = "Zeek"
  Product = "Zeek"
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """/syslog.log""" ]
  Fields = [
    """({time}\d{10})\.\d{6}(\t)?\s*({user_uid}[^\t\s]+)(\t)?\s*(({src_ip}({id_orig_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?)))|[^\t]+)(\t)?\s*(({id_orig_p}({src_port}\d+))|[^\t]+)(\t)?\s*(({dest_ip}({id_resp_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?)))|[^\t]+)(\t)?\s*(({id_resp_p}({dest_port}\d+))|[^\t]+)(\t)?\s*({protocol}[^\t\s]+)(\t)?\s*([^\t\s]+)(\t)?\s*({severity}[^\s\t]+)(\t)?\s*([^\t]+?)\s*$"""
# DL fields are removed
  ]


}
```