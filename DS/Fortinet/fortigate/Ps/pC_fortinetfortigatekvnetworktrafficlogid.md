#### Parser Content
```Java
{
Name = "fortinet-fortigate-kv-network-traffic-logid"
  Vendor = "Fortinet"
  Product = "FortiGate"
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """ vd=""", """ devname=""", """ devid=""", """ logid=""", """ level=""" ]
  Fields = [
    """eventtime=({time}\d{10})""",
# logtype is removed
    """\ssubtype="?({subtype}[^\s"]*)""",
    """\slogid="?({event_id}[^\s"]*)""",
    """\slevel="?({severity}[^=]+?)"?\s+(\w+=|$)""",
    """\sdevname="+(::ffff:)?({host}[^"\s]*)""",
    """\sdevid="+({device_id}[^"\s]*)""",
    """\saction="?({action}[^=]+?)"?\s+(\w+=|$)""",
    """\spolicyid=({policy_id}\d+)""",
    """\sdstip=(::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssrcip=(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\ssrcintf="?({src_interface}[^=]+?)"?\s+(\w+=|$)""",
    """\ssessionid=({session_id}[^\s]*)""",
    """\sservice="?({network_app}[^=]+?)"?\s+(\w+=|$)""",
    """\ssentpkt=({packets_out}\d+)""",
    """\ssentbyte=({bytes_out}\d+)""",
    """\srcvdbyte=({bytes_in}\d+)""",
    """\sproto=({protocol}[^\s]*)""",
    """\sduration=({duration}[^\s]*)""",
    """\sdstintf="?({dest_interface}[^=]+?)"?\s+(\w+=|$)""",
    """\sdstcountry="?({dest_country}[^=]+?)"?\s+(\w+=|$)""",
# appcat is removed
    """\ssrcport=({src_port}\d+)""",
    """\sdstport=({dest_port}\d+)""",
    """\ssrccountry="?({src_country}[^=]+?)"?\s+(\w+=|$)""",
    """\srcvdpkt=({packets_in}\d+)""",
# poluuid is removed
    """\suser="?\s*(N\/A|(?:host\/({src_host}[^"]+))|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)(@({domain}[^="]+))?)\s*"?\s+(\w+=|$)""",
# crscore is removed
# crlevel is removed
# craction is removed
    """\stransport=({src_translated_port}\d+)""",
    """\stransip=(::ffff:)?({src_translated_ip}[a-fA-F\d.:]+)""",
    """\smsg="?({additional_info}[^=]+?),?"?\s+(\w+=|$)""",
    """\slogdesc="+({event_name}[^"]+)""",
    """\sstatus="+({result}[^"\s]*)""",
    """\sreason="+({result_reason}[^"\s]*)""",
    """\sauthproto="+({protocol}[^\("]*)""",
    """\stranport=({src_translated_port}\d+)""",
    """\stranip=(::ffff:)?({dest_translated_ip}[a-fA-F\d.:]+)""",
    """\ssrcname="?(::ffff:)?({src_host}[\w\-.]+?)"?\s+\w+=""",
    """\ssrcmac="?({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})"?""",
    """\sosname=({os}[^\s]*)""",
    """\sosversion=({os_version}[^\s]*)""",
    """\sdevtype=({device_type}[^\s]*)""",
    """\sattack="?({attack}[^=]+?)"?\s+(\w+=|$)""",
    """\sattackid=({attack_id}\d+)""",
    """\sprofile="?({profile}[^=]+?)"?\s+(\w+=|$)""",
# trigger is removed
    """\sdirection="?({direction}[^=]+?)"?\s+(\w+=|$)""",
    """\sdevice="?({device_name}[^=]+?)"?\s+(\w+=|$)""",
    """\Wtz="?({tz}[+-]\d+)"""
  ]
  DupFields = [
    "bytes_in->bytes"
  ]


}
```