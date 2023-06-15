#### Parser Content
```Java
{
Name = zscaler-ia-json-network-traffic-success-internalreason
  ParserVersion = v1.0.0
  Vendor = Zscaler
  Product = Zscaler Internet Access
  TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
  Conditions = ["""InternalReason""" , """Client""", """IP""", """ConnectorZENSetupTime"""]
  Fields = [
     """Host":\s*"({host}[^"]+)"""",
     """({time}\w{3}\s\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
     """IPProtocol":\s*({protocol}[^"]+),"""
     """ServerIP":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
     """ConnectorPort":\s*({src_port}\d+),""",
     """ServerPort":\s*({dest_port}\d+),""",
     """Policy":\s*"\s*({policy_name}[^"]+)"""",
     """ConnectionStatus":\s*"({result}[^"]+)""""
     """"LogTimestamp":\s*"({time}[^"]+)""""
     """"SessionID":\s*"({session_id}[^"]+)""""
     """"ConnectionID":\s*"({connection_id}[^"]+)""""
     """"InternalReason":\s*"({result_reason}[^"]+)""""
     """"Username":\s*"(({email_address}[^"@]+?@[^"]+)|({user}[^"]+))""""
     """"ServicePort":\s*"({dest_port}\d+)""""
     """"ClientPublicIP":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
     """"ClientCountryCode":\s*"({src_country}[^"]+)""""
     """"ClientZEN":\s*"({zen_code}[^"]+)""""
     """"Connector":\s*"(0|({host}[^"]+))""""
     """"ConnectorZEN":\s*"({zen_con_code}[^"]+)""""
     """"ConnectorIP":\s*"({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
     """"Host":\s*"({dest_host}[^"]+)""""
     """"Application":\s*"({app}[^"]+)""""
     """"AppGroup":\s*"({app_group}[^"]+)""""
     """"TimestampConnectionStart":\s*"({event_start_time}[^"]+)""""
     """"TimestampConnectionEnd":\s*"({event_stop_time}[^"]+)""""
     """"ZENTotalBytesRxClient":\s*({rx_client_total_bytes}\d+)"""
     """"ZENTotalBytesTxClient":\s*({tx_client_total_bytes}\d+)"""
     """"ZENTotalBytesRxConnector":\s*({rx_connector_total_bytes}\d+)"""
     """"ZENTotalBytesTxConnector":\s*({tx_connector_total_bytes}\d+)"""
     """"PolicyProcessingTime":\s*({policy_runtime}\d+)"""
     """"CAProcessingTime":\s*({ca_runtime}\d+)"""
     """"AppLearnTime":\s*({app_learntime}\d+)"""
  ]
  DupFields = ["result->conn_status", "app_group->operation_type", "rx_connector_total_bytes->bytes_in", "tx_connector_total_bytes->bytes_out"]


}
```