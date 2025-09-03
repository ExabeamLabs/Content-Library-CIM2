#### Parser Content
```Java
{
Name = cisco-mma-kv-alert-trigger-airmarshalevents
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "epoch_sec"
  Conditions = [ """events type=""" ]
  Fields = [
    """({time}\d{10})\.\d*\s+({host}[\w.\-]+)\s+({alert_name}[^=]+?)\s+type=({event_name}.+?)\s+\w+=""",
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
    """\sip_src='({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
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
    """\ssrc='({src_mac}[^']+)""",
    """\sdst='({dest_mac}[^']+)""",
# wired_mac is removed
    """\svlan_id='({vlan_id}[^']+)""",
# rssi is removed
# fc_type is removed
    """original_server_ip='({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'""",
    """'Sess-ID\[({session_id}\d+)\]\s""",
    """\sUser\[(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\]:""",
    """\sUser\[[^\]]+\]:\s({additional_info}[^"]+?)(\s(Reason:\s({result_reason}[^']+?))?)\s*'""",
    """\sconn_id\[({connection_id}\d+)\]\s""",
    """\sBytes rcv:\s({bytes_in}\d+),\s"""
  ]
  DupFields = [ "event_name->alert_type" ]


}
```