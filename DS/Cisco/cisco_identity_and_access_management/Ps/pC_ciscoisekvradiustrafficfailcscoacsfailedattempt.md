#### Parser Content
```Java
{
Name = "cisco-ise-kv-radius-traffic-fail-cscoacsfailedattempt"
Vendor = "Cisco"
Product = "Cisco Identity and Access Management"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
  """ CSCOacs_Failed_Attempts """
]
Fields = [
  """\W({time}\w{3}\s+\d{1,2} \d\d:\d\d:\d\d)\s+({host}[\w\-.]+)\s"""
  """\"\w+\s+({time}\w+\s+\d{1,2}\s+\d\d:\d\d:\d\d\s+\d\d\d\d)\""""
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)"""
  """, User=({user}[\w\.\-\!\#\^\~]{1,40}\$?),"""
  """, UserName =(host\/)?(({domain}[^\s\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?),"""
  """, Calling-Station-ID=({dest_host}[^,]+)"""
  """, AD-User-Candidate-Identities=({dest_host}[^@,]+)"""
  """, AD-User-Candidate-Identities=({computer_name}[^@,]+)"""
  """, NetworkDeviceName =({network}[^,]+),"""
  """, Device IP Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """, DestinationIPAddress=({auth_server}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """, NetworkDeviceGroups=Location:All Locations:({location}[^,]+)"""
  """, FailureReason=({result_code}\d+)"""
  """\WFailed-Attempt:\s*({failure_reason}[^,]+),"""
]
ParserVersion = "v1.0.0"


}
```