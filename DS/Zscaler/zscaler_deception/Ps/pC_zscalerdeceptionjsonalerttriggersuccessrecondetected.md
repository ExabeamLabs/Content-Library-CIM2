#### Parser Content
```Java
{
Name = "zscaler-deception-json-alert-trigger-success-recondetected"
  ParserVersion = "v1.0.0"
  Vendor = "Zscaler"
  Product = "Zscaler Deception"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [
    """Zscaler Deception""",
    """"kill_chain_phase":"""",
    """Reconnaissance""",
    """abuseip""",
    """"decoy.type":"""",
    """recon"""
  ]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """"attacker.ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"decoy.ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"decoy.name":"({dest_host}[\w\-\.]+)"""",
    """"attacker.country":"({src_location}[^"]+)"""",
    """"abuseip.countryCode":"({country}[^"]+)"""",
    """"recon.method":"({method}[^"]+)"""",
    """"recon.scheme":"({protocol}[^"]+)"""",
    """"recon.request_uri":"({uri_path}[^"]+)"""",
    """"attacker.port":({src_port}\d+)""",
    """"recon.user_agent.string":"({user_agent}[^"]+)"""",
    """"severity":"({severity}[^"]+)"""",
    """"kill_chain_phase":"({category}[^"]+)"""",
    """"mitre_ids":({mitre_labels}[^\s]+),"severity":"({alert_severity}[^"]+)"""",
    """"type":"({alert_name}[^"]+)""""
  ]


}
```