#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-endpoint-login-userloginfail
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "epoch"
  ExtractionType = json
  Conditions = [ """"event_simpleName":"UserLogonFailed""" ]
  Fields = [
    """"timestamp":\s*"*({time}\d{13})"""",
    """"UserName":\s*"(-|\/+|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({full_name}({first_name}[^\s"@]+)\s({last_name}[^"]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """"UserSid":\s*"({user_sid}[^"]+)"""",
    """"event_simpleName":"({event_code}[^"]+)""",
    """"aid":"({aid}[^"]+)""",
    """"aip":\s*"({aip}[a-fA-F:\d.]+)"""",
    """"LogonType":"({login_type}\d+)"""",
    """"name":"({event_name}[^"]+)"""",
    """"LogonDomain":"\s*({domain}[^\"]+?)\s*"""",
    """"ClientComputerName":"(-|({src_host}[\w\-\.]+))"""",
    """"RemoteAddressIP4":"({src_ip}[A-Fa-f:\d\.]+)"""",
    """"cid":"({cid}[^"]+)"""
    """"event_platform":"({os}[^"]+)""""
    """"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"ComputerName":"({host}[\w\-\.]+)""""
    """exa_json_path=$.ProcessStartTime,exa_field_name=time""",
    """exa_json_path=$.UserName,exa_regex=^(-|\/+|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({full_name}({first_name}[^\s"@]+)\s({last_name}[^"]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\"]+))?)$""",
    """exa_json_path=$..timestamp,exa_field_name=time""",
    """exa_json_path=$.raw-event.timestamp,exa_field_name=time""",
    """exa_json_path=$..UserName,exa_regex=(-|\/+|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({full_name}({first_name}[^\s"@]+)\s({last_name}[^"]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$..UserSid,exa_field_name=user_sid""",
    """exa_json_path=$..event_simpleName,exa_field_name=event_code""",
    """exa_json_path=$..aid,exa_field_name=aid""",
    """exa_json_path=$..aip,exa_field_name=aip""",
    """exa_json_path=$..LogonType,exa_field_name=login_type""",
    """exa_json_path=$..name,exa_field_name=event_name""",
    """exa_regex="LogonDomain":"\s*({domain}[^\"]+?)\s*"""",
    """exa_json_path=$..ClientComputerName,exa_regex=^(-|({src_host}[\w\-\.]+))$""",
    """exa_json_path=$..RemoteAddressIP4,exa_regex=({src_ip}[A-Fa-f:\d\.]+)"""
    """exa_json_path=$..event_platform,exa_field_name=os""",
    """exa_json_path=$..cid,exa_field_name=cid""",
    """exa_json_path=$.LocalAddressIP4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.ComputerName,exa_regex=({host}[\w\-\.]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```