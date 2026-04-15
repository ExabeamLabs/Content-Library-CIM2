#### Parser Content
```Java
{
Name = pan-ngfw-json-app-activity-success-userid-catchall
 Conditions = [ """"LogType":"USERID"""", """"Subtype":"""" ]
 ParserVersion = "v1.0.0"

paloalto-vpn-event = {
   Vendor = Palo Alto Networks
   Product = GlobalProtect
   TimeFormat = "epoch"
   Fields = [
       """\srt=({time}\d{13})""",
       """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
       """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
       """\ssuser=(({domain}[^\\=]+?)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+=""",
       """\sdvchost=({host}[\w\-.]+?)\s+\w+=""",
       """\scs2=({result}[^=]+)\s+\w+=""",
       """\smsg=({event_name}[^=]+?)\s+\w+=""",
       """cs6=({os}[^=]+?)\s+\w+=""",
       """sourceGeoCountryCode=({src_country}[^=]+?)\s+\w+=""",
       """({app}GLOBALPROTECT)"""
     ]
 },

cef-palo-alto-networks-firewall = {
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = ["epoch", "MMM dd yyyy HH:mm:ss z", "MMM dd yyyy HH:mm:ss", "yyyy/MM/dd HH:mm:ss","epoch_sec"]
  Fields = [
    """\sdvchost=({host}.+?)\s+(\w+=|$)""",
    """\Wrt=({time}\d+\/\d+\/+\d+\s+\d+:\d+:\d+)"""
    """\Wrt=({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+)\s+\w+""",
    """\Wrt=({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+\s+\w+)\s+\w+(:|=)""",
    """\srt=({time}\d{10})\s+(\w+=|$)"""
    """\srt=({time}\d{13})\s+(\w+=|$)""",
    """\sduser=(?=[^\s]+@[^\s]+)({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s@]+)\s+(\w+=|$)""",
    """\sduser=(?!\S+@\S+)(({domain}[^\\\s]+)?\\+)?(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)""",
    """\ssuser=(?=[^\s]+@[^\s]+)({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s@]+)\s+(\w+=|$)""",
    """\ssuser=(?!\S+@\S+)(({domain}[^\\\s]+)?\\+)?(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)""",
    """({event_category}TRAFFIC)""",
    """\|({subtype}[^\|]+)\|TRAFFIC""",
    """\scs1=({rule}.+?)\s+(\w+=|$)""",
    """\sshost=({src_host}.+?)\s+(\w+=|$)""",
    """\sdhost=({dest_host}.+?)\s+(\w+=|$)""",
    """\ssrc=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+(\w+=|$)""",
    """\sdst=(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s+(\w+=|$)""",
    """\ssourceTranslatedAddress=(0.0.0.0|({src_translated_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}))\s+(\w+=|$)""",
    """\sdestinationTranslatedAddress=(0.0.0.0|({dest_translated_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}))\s+(\w+=|$)""",
    """\sspt=(0|({src_port}\d+))\s+(\w+=|$)""",
    """\sdpt=(0|({dest_port}\d+))\s+(\w+=|$)""",
    """\ssourceTranslatedPort=(0|({src_translated_port}\d+))\s+(\w+=|$)""",
    """\sdestinationTranslatedPort=(0|({dest_translated_port}\d+))\s+(\w+=|$)""",
    """\sapp=({network_app}.+?)\s+(\w+=|$)""",
    """\scs4=({src_network_zone}.+?)\s+(\w+=|$)""",
    """\scs5=({dest_network_zone}.+?)\s+(\w+=|$)""",
    """\scs6=({profile}.+?)\s+(\w+=|$)""",
    """\sproto=({protocol}.+?)\s+(\w+=|$)""",
    """\sin=({bytes_in}[\d.]+)\s+(\w+=|$)""",
    """\sout=({bytes_out}[\d.]+)\s+(\w+=|$)""",
    """\scs2=({category}.+?)\s+(\w+=|$)""",
    """\sseverity=({severity}.+?)\s+(\w+=|$)""",
    """\sdeviceDirection=({direction}.+?)\s+(\w+=|$)""",
    """\scategoryOutcome=\/?({result}.+?)\s+(\w+=|$)""",
    """\sreason=(?:n\/a|({result_reason}.+?))\s+(\w+=|$)"""
    """act=({action}.+?)\s+(\w+=|$)""",
  paloalto-vpn = {
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  ExtractionType = json
  Fields = [
  """exa_json_path=$.TimeGenerated,exa_field_name=time"""
  """exa_json_path=$.host,exa_regex=^({host}[\w.-]+)$"""
  """exa_json_path=$.host,exa_regex=^({firewall}[\w.-]+)$"""
  """exa_json_path=$.DeviceName,exa_regex=^({host}[\w.-]+)$"""
  """exa_json_path=$.DeviceName,exa_field_name=device_name"""
  """exa_json_path=$.DeviceName,exa_regex=^({firewall}[\w.-]+)$"""
  """exa_json_path=$.PrivateIPv6,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.PrivateIPv4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.PublicIPv4,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.PublicIPv6,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.LogType,exa_field_name=app"""
  """exa_json_path=$.EventStatus,exa_field_name=result"""
  """exa_json_path=$.EndpointDeviceName,exa_field_name=src_host"""
  """exa_json_path=$.SourceRegion,exa_field_name=src_country"""
  """exa_json_path=$.SourceUserName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """exa_regex=(Source)?User(Name)?":"((na|NA|({domain}[^"\\]+))\\+)?(({email_address}[^@"]+@[^\."]+\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """exa_json_path=$.EndpointOSType,exa_field_name=os"""
  """exa_json_path=$.EventIDValue,exa_field_name=event_name"""
  """exa_json_path=$.EventIDValue,exa_field_name=auth_method"""
  """exa_json_path=$.SourcePort,exa_field_name=src_port"""
  """exa_json_path=$.DestinationPort,exa_field_name=dest_port"""
  """exa_json_path=$.Protocol,exa_field_name=protocol"""
  """exa_json_path=$.LogType,exa_field_name=event_category"""
  """exa_json_path=$.EndpointOSVersion,exa_field_name=os"""
  """exa_json_path=$.DestinationAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.event.DestinationAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.event.TimeGenerated,exa_field_name=time"""
  """exa_json_path=$.event.host,exa_regex=^({host}[\w.-]+)$"""
  """exa_json_path=$.event.host,exa_regex=^({firewall}[\w.-]+)$"""
  """exa_json_path=$.event.DeviceName,exa_regex=^({host}[\w.-]+)$"""
  """exa_json_path=$.event.DeviceName,exa_field_name=device_name"""
  """exa_json_path=$.event.DeviceName,exa_regex=^({firewall}[\w.-]+)$"""
  """exa_json_path=$.event.PrivateIPv6,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.event.PrivateIPv4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.event.PublicIPv4,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.event.PublicIPv6,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$.event.LogType,exa_field_name=app"""
  """exa_json_path=$.event.EventStatus,exa_field_name=result"""
  """exa_json_path=$.event.EndpointDeviceName,exa_field_name=src_host"""
  """exa_json_path=$.event.SourceRegion,exa_field_name=src_country"""
  """exa_json_path=$.event.SourceUserName,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """exa_json_path=$.event.EndpointOSType,exa_field_name=os"""
  """exa_json_path=$.event.EventIDValue,exa_field_name=event_name"""
  """exa_json_path=$.event.EventIDValue,exa_field_name=auth_method"""
  """exa_json_path=$.event.SourcePort,exa_field_name=src_port"""
  """exa_json_path=$.event.DestinationPort,exa_field_name=dest_port"""
  """exa_json_path=$.event.Protocol,exa_field_name=protocol"""
  """exa_json_path=$.event.LogType,exa_field_name=event_category"""
  """exa_json_path=$.event.EndpointOSVersion,exa_field_name=os"""
  """exa_regex=Source(Address|IP)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$.event.Description,exa_field_name=additional_info"""
  """exa_regex=((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
    """exa_json_path=$.Action,exa_field_name=action"""
    """exa_json_path=$.NATSource,exa_regex=({src_translated_ip}[a-fA-F\d:.]+)"""
    """exa_json_path=$.NATDestination,exa_regex=({dest_translated_ip}[a-fA-F\d:.]+)"""
    """exa_json_path=$.NATSourcePort,exa_field_name=src_translated_port"""
    """exa_json_path=$.NATDestinationPort,exa_field_name=dest_translated_port"""
    """exa_json_path=$.Bytes,exa_field_name=bytes"""
    """exa_json_path=$.BytesSent,exa_field_name=bytes_out"""
    """exa_json_path=$.BytesReceived,exa_field_name=bytes_in"""
    """exa_json_path=$.URLCategory,exa_field_name=category"""
    """exa_json_path=$.Rule,exa_field_name=alert_name"""
    """exa_json_path=$.VendorSeverity,exa_field_name=alert_severity"""
    """exa_json_path=$.LogType,exa_field_name=alert_type"""
    """exa_json_path=$.Subtype,exa_field_name=alert_type"""
    """exa_json_path=$.Application,exa_field_name=network_app"""
    """exa_json_path=$.FromZone,exa_field_name=src_network_zone"""
    """exa_json_path=$.ToZone,exa_field_name=dest_network_zone"""
    """exa_json_path=$.event.NATSource,exa_regex=({src_translated_ip}[a-fA-F\d:.]+)"""
    """exa_json_path=$.event.NATDestination,exa_regex=({dest_translated_ip}[a-fA-F\d:.]+)"""
    """exa_json_path=$.event.NATSourcePort,exa_field_name=src_translated_port"""
    """exa_json_path=$.event.NATDestinationPort,exa_field_name=dest_translated_port"""
    """exa_json_path=$.event.Bytes,exa_field_name=bytes"""
    """exa_json_path=$.event.BytesSent,exa_field_name=bytes_out"""
    """exa_json_path=$.event.BytesReceived,exa_field_name=bytes_in"""
    """exa_json_path=$.event.URLCategory,exa_field_name=category"""
    """exa_json_path=$.event.Rule,exa_field_name=alert_name"""
    """exa_json_path=$.event.VendorSeverity,exa_field_name=alert_severity"""
    """exa_json_path=$.event.LogType,exa_field_name=alert_type"""
    """exa_json_path=$.event.Subtype,exa_field_name=alert_type"""
    """exa_json_path=$.event.Application,exa_field_name=network_app"""
    """exa_json_path=$.event.FromZone,exa_field_name=src_network_zone"""
    """exa_json_path=$.event.ToZone,exa_field_name=dest_network_zone"""
    """exa_json_path=$.Rule,exa_field_name=rule"""
    """exa_json_path=$.ThreatName,exa_field_name=alert_name"""
    """exa_json_path=$.InboundInterface,exa_field_name=src_interface"""
    """exa_json_path=$.OutboundInterface,exa_field_name=dest_interface"""
    """exa_json_path=$.event.InboundInterface,exa_field_name=src_interface"""
    """exa_json_path=$.event.OutboundInterface,exa_field_name=dest_interface"""
    """exa_json_path=$.event.Action,exa_field_name=action"""
    """exa_json_path=$.event.ThreatCategory,exa_regex=((?i:unknown)|({threat_category}[^"]+))"""
    """exa_json_path=$.event.ThreatID,exa_regex=({alert_name}[^"\(]+?)\s*(\(({alert_id}[^"\)]\d+))"""
  ]
}
}
```