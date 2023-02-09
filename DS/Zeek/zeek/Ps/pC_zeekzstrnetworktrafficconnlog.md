#### Parser Content
```Java
{
Name = zeek-z-str-network-traffic-connlog
  ParserVersion = v1.0.0
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """/conn.log""" ]
  Fields = [
    """({time}\d{10})\.\d{6}\s+({user_id}[^\s]+)\s+(({id_orig_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+)\s+((({id_orig_p}\d+?)|[^\s]+)\s+|[^\s]+)\s+(({id_resp_h}(\d{1,3}\.){3}\d{1,3}|(([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\s]+)\s+|[^\s]+)\s+(({id_resp_p}\d+?)|[^\s]+)\s+({protocol}[^\s]+)\s+({service_name}[^\s]+)\s+({duration}[^\s]+)\s+({orig_bytes}\d*)\s+({resp_bytes}\d*)\s+({connection_state}[^\s]+)\s+({local_orig}[^\s]+)\s+({local_resp}[^\s]+)\s+({missed_bytes}\d*)\s+({history}[^\s]+)\s+({orig_pkts}[^\s]+)\s+({orig_ip_bytes}[^\s]+)\s+({resp_pkts}\d*)\s+({resp_ip_bytes}[^\s]+)\s+({tunnel_parents}[^\s]+)\s*"""
    """\d+\.\d{6}\s+([^\s]+\s){20}({orig_cc}[^\s]+)\s+({resp_cc}[^\s]+)\s+({sensorname}[^\s]+)\s*"""
  ]
  DupFields = [ "id_orig_h->src_ip", "id_orig_p->src_port", "id_resp_h->dest_ip", "id_resp_p->dest_port", "sensorname->src_interface", "orig_ip_bytes->bytes_out", "resp_ip_bytes->bytes_in" ]


}
```