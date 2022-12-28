#### Parser Content
```Java
{
Name = zeek-z-str-network-traffic-weird
  Vendor = Zeek
  Product = Zeek 
  TimeFormat = "epoch_sec"
  Conditions = [ """/weird.log""" ]
  Fields = [

        """({time}\d{10})\.\d{6}\s+({user_uid}[^\s]+)\s+(({id_orig_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+)\s+(({id_orig_p}\d+?)|[^\s]+)\s+(({id_resp_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+)\s+(({id_resp_p}\d+?)|[^\s]+)\s+({event_name}[^\s]+)\s+([^\s]+)\s+([^\s]+)\s+([^\s]+?)\s*"""
# addl is removed
   """({time}\d{10})\.\d{6}\t({user_uid}[^\t]+)\t(({id_orig_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\t]+)\t(({id_orig_p}\d+?)|[^\t]+)\t(({id_resp_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\t]+)\t(({id_resp_p}\d+?)|[^\t]+)\t({event_name}[^\t]+)\t([^\t]+)\t([^\t]+)\t([^\t]+?)\s*$""" 
# addl is removed
  ]
  DupFields = [ "id_orig_h->src_ip", "id_orig_p->src_port", "id_resp_h->dest_ip", "id_resp_p->dest_port", "name->additional_info" ]
  ParserVersion = "v1.0.0"


}
```