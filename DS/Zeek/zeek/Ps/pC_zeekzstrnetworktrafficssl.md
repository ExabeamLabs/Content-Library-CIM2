#### Parser Content
```Java
{
Name = zeek-z-str-network-traffic-ssl
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """/ssl.log""" ]
  Fields = [
   """({time}\d{10})\.\d{6}\t({user_uid}[^\t]+)\t(({src_ip}({id_orig_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?)))|[^\t]+)\t(({id_orig_p}({src_port}\d+?))|[^\t]+)\t(({dest_ip}({id_resp_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?)))|[^\t]+)\t(({id_resp_p}({dest_port}\d+?))|[^\t]+)\t({service_name}({version}[^\t]+))\t({auth_method}({cipher}[^\t]+))\t([^\t]+)\t({server_name}[^\t]+)\t([^\t]+)\t([^\t]+)\t([^\t]+)\t([^\t]+)\t([^\t]+)\t([^\t]+)\t({client_cert_subject}[^\t]+)\t([^\t]+)\t([^\t]+)\t([^\t]+)\t([^\t]+?)\s*$"""
# DL Fields are removed
  ]
  ParserVersion = "v1.0.0"


}
```