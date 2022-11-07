#### Parser Content
```Java
{
Name = zeek-z-kv-database-query-success-tquery
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """/mysql.log""", """\tquery\t""" ]
  Fields = [
     """((([Fa-f0-9%.:]+(th0)?))|[^\t]+)\t(({id_orig_p}\d+?)|[^\t]+)\t(({id_resp_h}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|[^\t]+)\t(({id_resp_p}\d+?)|[^\t]+)\t([^\t]+)\t({arg}[^\t]+)\t([^\t]+)\t([^\t]+)\t({response}[^\t]+?)\s*$"""
# DL Fields are removed
  ]
  DupFields = [ "id_orig_h->src_ip", "id_orig_p->src_port", "id_resp_h->dest_ip", "id_resp_p->dest_port", "arg->db_query" ]
  ParserVersion = "v1.0.0"


}
```