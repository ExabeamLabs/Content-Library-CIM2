#### Parser Content
```Java
{
Name = "zscaler-pa-json-app-notification-connector-status"
Vendor = "Zscaler"
Product = "Zscaler Private Access"
ParserVersion = "v1.0.0"
TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
Conditions = [ """"ZEN":""", """"SessionType":""", """ZPN_ASSISTANT_""", """BROKER""", """"SessionStatus":""", """"Connector":""" ]
Fields = [
  """"LogTimestamp":"({time}[^"]+)"""",
  """"SessionID":\s*"({session_id}[^"]+)"""",
  """"PublicIP":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
  """"PrivateIP":\s*"({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""", 
  """"TotalBytesRx":\s*({bytes_in}\d+)""",
  """"TotalBytesTx":\s*({bytes_out}\d+)""",
  """"SessionStatus":\s*"({event_name}[^\"]+)"""",
  """"CountryCode":\s*"({src_country}[^"]+)"""",
  """"Connector":\s*"(0|({host}[^"]+))"""",
  """"RequestSize":\s*({bytes_out}\d+)""",
  """"ResponseSize":\s*({bytes_in}\d+)""",
  """"Platform":\s*"({os}.+?)"""",
  """"NameID":"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))""""
]


}
```