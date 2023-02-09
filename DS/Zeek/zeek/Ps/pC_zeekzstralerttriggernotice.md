#### Parser Content
```Java
{
Name = zeek-z-str-alert-trigger-notice
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = ["""/notice.log""" ]
  Fields = [

    """({time}\d{10})\.\d{6}\s+({user_uid}[^\s]+)\s+(({id_orig_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+)\s+(({id_orig_p}\d+?)|[^\s]+)\s+(({id_resp_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+)\s+(({id_resp_p}\d+?)|[^\s]+)\s+([^\s]+)\s+([^\s]+)\s+([^\s]+)\s+({protocol}[^\s]+)\s+([^\s]+)\s+([^\s]+)\s+([^\s]+)\s+([^\s]+)\s+([^\s]+)\s+([^\s]+)\s+([^\s]+)\s+([^\s]+)\s+({action}[^\s]+)\s+([^\s]+)\s+([^\s]+)\s+({remote_location_country_code}[^\s]+)\s+({remote_location_region}[^\s]+)\s+({remote_location_city}[^\s]+)\s+({remote_location_latitude}[^\s]+)\s+({remote_location_longitude}[^\s]+?)\s*"""
# DL fields are removed
  ]
  DupFields = [ "id_orig_h->src_ip", "id_orig_p->src_port", "id_resp_h->dest_ip", "id_resp_p->dest_port",  "msg->failure_reason", "peer_descr->dest_interface" ]
  ParserVersion = "v1.0.0"


}
```