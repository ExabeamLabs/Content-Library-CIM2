#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-app-notification-success-kextload
  ParserVersion = v1.0.0
  Conditions = [ """"aid":""", """"aip":""", """"event_simpleName":"KextLoad"""", """"event_platform":""" ]

crowdstrike-json-app-notification = {
  Vendor = CrowdStrike
  Product = Falcon
  ExtractionType = json
  TimeFormat = "epoch"
  Fields = [
    """"eventCreationTime":({time}\d{13})""",
    """"timestamp":\s*"*({time}\d{13})""",
    """"aid":\s*"({aid}[^"]+)""",
    """"UserName":\s*"({user}[\w\.\-]{1,40}\$?)""""
    """"aip":\s*"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"name":\s*"({alert_type}[^"]+)"""
    """"ClientComputerName":\s*"({src_host}[^"]+)"""
    """"event_platform":\s*"({os}[^"]+)""",
    """"UserSid":\s*"({user_sid}[^"]+)""",
    """"RemoteAddressIP4":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"destinationServiceName":"({app}CrowdStrike)""""
    """"LogonDomain":"(NT AUTHORITY|({domain}[^\"]+))""",
    """exa_regex="eventCreationTime":({time}\d{13})""",
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.aid,exa_field_name=aid""",
    """exa_json_path=$.UserPrincipal,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_regex="UserName":\s*"({user}[\w\.\-]{1,40}\$?)"""",
    """exa_json_path=$.aip,exa_regex=({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.name,exa_field_name=alert_type""",
    """exa_json_path=$.ClientComputerName,exa_field_name=src_host""",
    """exa_json_path=$.event_platform,exa_field_name=os""",
    """exa_json_path=$.cid,exa_field_name=cid""",
    """exa_json_path=$.UserSid,exa_field_name=user_sid""",
    """exa_json_path=$.RemoteAddressIP4,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.destinationServiceName,exa_field_name=app""",
    """exa_json_path=$.LogonDomain,exa_field_name=domain"""
  
}
```