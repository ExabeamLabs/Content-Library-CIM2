#### Parser Content
```Java
{
Name = zeek-zeek-str-network-traffic-tunnellog
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """/tunnel.log""" ]
  Fields = [
    """({time}\d{10})\.\d{6}[\t\s]*({user_uid}[^\t\s]+)[\t\s]*(({id_orig_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\t\s]+)[\t\s]*(({id_orig_p}\d+?)|[^\t\s]+)[\t\s]*(({id_resp_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\t\s]+)[\t\s]*(({id_resp_p}\d+)|[^\t\s]+)[\t\s]*({vpn_client_type}[^\t\s]+)[\t\s]*({action}[^\t]+?)("|\s*$)"""
  ]
  DupFields = [ "id_orig_h->src_ip", "id_orig_p->src_port", "id_resp_h->dest_ip", "id_resp_p->dest_port" ]


}
```