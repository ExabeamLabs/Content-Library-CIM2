#### Parser Content
```Java
{
Name = sophos-xgfirewall-kv-network-traffic-success-firewallrule
  ParserVersion = v1.0.0
  Vendor = Sophos
  Product = Sophos XG Firewall
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","yyyy-MM-dd' time='HH:mm:ss"]
  Conditions = [ """device_name=""", """"SFW"""", """log_component="Firewall Rule""", """status=""""]
  Fields = [
    """timestamp="({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}(\+|\-)[\d:]+)""",
    """date=({time}\d{4}-\d\d-\d\d\stime=\d\d:\d\d:\d\d)""",
    """\sdevice_name="(SFW|({host}\S+))?"\s""",
    """\s(device_id|device_serial_id)="?({device_id}\S*?)"?\s""",
    """\slog_id="?({event_id}\S+?)"?\s""",
    """\slog_type="({event_category}\S+)?"\s""",
    """\slog_subtype="({action}({subtype}\S+))?"\s""",
    """\sstatus="({action}\S+)?"\s""",
    """\spriority=({priority}\S+)?\s""",
    """\sduration=({duration}\d+)?\s""",
    """\sfw_rule_id=({rule_id}\d+)?\s""",
    """\spolicy_type=({policy_name}\S+)?\s""",
    """\suser_name="(({user}[\w\.\-]{1,40}\$?)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))?"\s.*?\s""",
    """\sin_interface="({src_interface}\S+)?"\s""",
    """\sout_interface="({dest_interface}\S+)?"\s""",
    """\ssrc_mac="?({src_mac}\S+?)"?\s""",
    """\sdst_mac="?({dest_mac}\S+?)"?\s""",
    """\ssrc_ip="?({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})?"?\s""",
    """\ssrc_country_code=({src_country_code}\S+)?\s""",
    """\sdst_ip="?({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})?"?\s""",
    """\sdst_country_code=({dest_county_code}\S+)?\s""",
    """\sprotocol="({protocol}\S+)?"\s""",
    """\ssrc_port=({src_port}\d+)?\s""",
    """\sdst_port=({dest_port}\d+)?\s""",
    """\s(tran_src_ip|src_trans_ip)=({src_translated_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})?\s""",
    """\s(tran_src_port|src_trans_port)=({src_translated_port}\d+)?\s""",
    """\s(tran_dst_ip|dst_trans_ip)=({dest_translated_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})?\s""",
    """\s(tran_dst_port|dst_trans_port)=({dest_translated_port}\d+)?\s""",
    """\ssrc_zone="({src_network_zone}[^"]+)""""
    """\sdst_zone="({dest_network_zone}[^"]+)""""
    """\ssrc_country="({src_country}[^"]+)""""
    """\sdst_country="({dest_country}[^"]+)""""
  ]


}
```