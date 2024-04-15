#### Parser Content
```Java
{
Name = "zscaler-pa-json-vpn-login-success-doubleencryption"
Vendor = "Zscaler"
Product = "Zscaler Private Access"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
"""ZENBytesRxConnector"""
"""ZENTotalBytesTxConnector"""
"""ZENBytesTxConnector"""
"""TimestampZENLastRxClient"""
"""DoubleEncryption"""
]
Fields = [
"""Host":\s*"({host}[^"]+)""""
"""({time}\w{3}\s\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)"""
"""Username":\s*"(({email_address}[^@]+@[^"]*)|({user}[^"]+))""""
"""Username":\s*"(({email_address}[^@\"\s]+@[^\s\"]*)|({user}[^"]+))"""
"""IPProtocol":\s*({protocol}[^,]+),"""
"""ClientPublicIP":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""ServerIP":\s*"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
"""ConnectorPort":\s*({src_port}\d+),"""
"""ServerPort":\s*({dest_port}\d+),"""
"""Application":\s*"\s*({app}[^"]+)""""
"""AppGroup":\s*"\s*({operation_type}[^"]+)""""
"""ZENTotalBytesRxConnector":\s*({bytes_in}\d+),"""
"""ZENTotalBytesTxConnector":\s*({bytes_out}\d+),"""
"""Policy":\s*"\s*({policy_name}[^"]+)""""
"""ConnectionStatus":\s*"({result}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```