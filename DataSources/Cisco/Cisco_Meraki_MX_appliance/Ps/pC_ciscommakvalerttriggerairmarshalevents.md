#### Parser Content
```Java
{
Name = cisco-mma-kv-alert-trigger-airmarshalevents
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco Meraki MX appliance
  TimeFormat = "epoch_sec"
  Conditions = [ """events type=""" ]
  Fields = [
    """({time}\d+)\.\d*\s+({host}[\w.\-]+)\s+({alert_name}[^=]+?)\s+type=({event_name}.+?)\s+\w+=""",
# radio is removed
# vap is removed
    """\sclient_mac='({src_mac}[^']+)""",
    """\schannel='({channel}[^']+)""",
# instigator is removed
    """\sduration='({duration}[^']+)""",
# auth_neg_dur is removed
# last_auth_ago is removed
    """\sis_8021x='({is_8021x}[^']+)""",
# full_conn is removed
# ip_resp is removed
    """\sip_src='({src_ip}[^']+)""",
# http_resp is removed
# arp_resp is removed
# arp_src is removed
# dns_server is removed
# dns_req_rtt is removed
# dns_resp is removed
# dhcp_lease_completed is removed
    """\sdhcp_ip='({dhcp_ip}[^']+)""",
# dhcp_server is removed
# dhcp_server_mac is removed
# dhcp_resp is removed
# identity is removed
    """\said='({aid}[^']+)""",
    """\sssid='({ssid}[^']+)""",
# bssid is removed
    """\ssrc='({src_ip}[^']+)""",
    """\sdst='({dest_ip}[^']+)""",
# wired_mac is removed
    """\svlan_id='({vlan_id}[^']+)""",
# rssi is removed
# fc_type is removed
  ]
  DupFields = [ "dest_ip->user" , "event_name->alert_type" ]


}
```