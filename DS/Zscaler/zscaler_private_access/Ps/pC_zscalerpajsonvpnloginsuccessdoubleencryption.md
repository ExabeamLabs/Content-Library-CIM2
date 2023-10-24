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
""""Username":\s*"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?)|({full_name}[^",]+))""""
"""Username":\s*"(({email_address}[^@\"\s]+@[^\s\"]*)|({user}[\w\.\-]{1,40}\$?)|({full_name}[^",]+))""""
""""Username":\s*\"(({email_address}[^@\"\s]+@[^\s\"]*)|((({domain}[^@\"]+)@)?({user}[\w\.\-]{1,40}\$?))|({full_name}[^\"@]+))""""
"""IPProtocol":\s*({protocol}[^,]+),"""
"""ClientPublicIP":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""ServerIP":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
"""ConnectorPort":\s*({src_port}\d+),"""
"""ServerPort":\s*({dest_port}\d+),"""
"""Application":\s*"\s*({app}[^"]+)""""
"""AppGroup":\s*"\s*({operation_type}[^"]+)""""
"""ZENTotalBytesRxConnector":\s*({bytes_in}\d+),"""
"""ZENTotalBytesTxConnector":\s*({bytes_out}\d+),"""
"""Policy":\s*"\s*({policy_name}[^"]+)""""
"""ConnectionStatus":\s*"({result}[^"]+)""""
""""InternalReason":\s*"({reason}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```