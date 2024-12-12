#### Parser Content
```Java
{
Name = "zscaler-pa-json-vpn-login-success-doubleencryption"
Vendor = "Zscaler"
Product = "Zscaler Private Access"
TimeFormat = "MMM dd HH:mm:ss yyyy"
ExtractionType = json
Conditions = [
"""ZENBytesRxConnector"""
"""ZENTotalBytesTxConnector"""
"""ZENBytesTxConnector"""
"""DoubleEncryption"""
]
Fields = [
  """Host":\s*"({host}[^"]+)""""
  """({time}\w{3}\s\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)"""
  """"Username":\s*"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^",]+))""""
  """Username":\s*"(({email_address}[^@\"\s]+@[^\s\"]*)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^",]+))""""
  """"Username":\s*\"(({email_address}[^@\"\s]+@[^\s\"]*)|((({domain}[^@\"]+)@)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({full_name}[^\"@]+))""""
  """IPProtocol":\s*({protocol}[^,]+),"""
  """ClientPublicIP":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """ServerIP":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  """ConnectorPort":\s*({src_port}\d+),"""
  """ServerPort":\s*({dest_port}\d+),"""
  """Application":\s*"\s*({app}[^"]+)""""
  """AppGroup":\s*"\s*({app_group}[^"]+?)\s*("|\w+=|$)"""
  """ZENTotalBytesRxConnector":\s*({bytes_in}\d+),"""
  """ZENTotalBytesTxConnector":\s*({bytes_out}\d+),"""
  """Policy":\s*"\s*({policy_name}[^"]+)""""
  """ConnectionStatus":\s*"({result}[^"]+)""""
  """"InternalReason":\s*"({result_reason}[^"]+)""""
  """ClientCountryCode":\s*"({country_code}.+?)""""
  """"ConnectorIP":\s*"({proxy_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  """exa_json_path=$..Host,exa_field_name=host""",
  """exa_json_path=$.metadata.source.host,exa_field_name=host"""
  """exa_json_path=$..LogTimestamp,exa_regex=({time}\w{3}\s\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
  """exa_json_path=$..Username,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)"|({full_name}[^",]+))"""
  """exa_json_path=$..IPProtocol,exa_field_name=protocol""",
  """exa_json_path=$..ClientPublicIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """exa_json_path=$..ServerIP,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """exa_json_path=$..ConnectorPort,exa_field_name=src_port""",
  """exa_json_path=$..ServerPort,exa_field_name=dest_port""",
  """exa_json_path=$..Application,exa_regex=^\s*({app}[^"]+?)$"""
  """exa_json_path=$..AppGroup,exa_regex=^\s*({app_group}[^"]+?)\s*$"""
  """exa_json_path=$..ZENTotalBytesRxConnector,exa_field_name=bytes_in""",
  """exa_json_path=$..ZENTotalBytesTxConnector,exa_field_name=bytes_out""",
  """exa_json_path=$..Policy,exa_regex=^\s*({policy_name}[^"]+?)$"""
  """exa_json_path=$..ConnectionStatus,exa_field_name=result""",
  """exa_json_path=$..InternalReason,exa_field_name=result_reason""",
  """exa_json_path=$..ClientCountryCode,exa_field_name=country_code""",
  """exa_json_path=$..ConnectorIP,exa_regex=({proxy_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
]
ParserVersion = "v1.0.0"


}
```