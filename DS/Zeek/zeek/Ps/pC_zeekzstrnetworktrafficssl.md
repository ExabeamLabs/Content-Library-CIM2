#### Parser Content
```Java
{
Name = zeek-z-str-network-traffic-ssl
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """/ssl.log""" ]
  Fields = [
   """({time}\d{10})\.\d{6}\t({user_uid}[^\t]+)\t(({id_orig_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\t]+)\t(({id_orig_p}\d+?)|[^\t]+)\t(({id_resp_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\t]+)\t(({id_resp_p}\d+?)|[^\t]+)\t({version}[^\t]+)\t({cipher}[^\t]+)\t([^\t]+)\t({server_name}[^\t]+)\t([^\t]+)\t([^\t]+)\t([^\t]+)\t([^\t]+)\t([^\t]+)\t([^\t]+)\t({client_cert_subject}[^\t]+)\t([^\t]+)\t([^\t]+)\t([^\t]+)\t([^\t]+?)\s*$"""
# DL Fields are removed
  ]
  DupFields = [ "id_orig_h->src_ip", "id_orig_p->src_port", "id_resp_h->dest_ip", "id_resp_p->dest_port", "version->service_name", "cipher->auth_method" ]
  ParserVersion = "v1.0.0"


}
```