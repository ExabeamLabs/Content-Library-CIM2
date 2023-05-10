#### Parser Content
```Java
{
Name = microsoft-defenderep-cef-endpoint-login-interactive
  ParserVersion = v1.0.0
  Conditions = [ """AdvancedHunting-DeviceLogonEvents""", """"LogonType":"Interactive"""", """"InitiatingProcessParentFileName":""" ]

cef-defender-atp-events = {
    Vendor = Microsoft
    Product = Microsoft Defender for Endpoint
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
    Fields = [
      """"time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """"DeviceName":"({host}[^"]+)""""
      """"LogonType":"({login_type_text}[^"]+)"""",
      """"AccountName":"({user}[^"]+)"""",
      """"AccountDomain":"({domain}[^"]+)"""",
      """"InitiatingProcessFileName":"({process_name}[^"]+)"""",
      """"category":"({event_name}[^"]+)"""",
      """"ActionType":"({action}[^"]+)"""",
      """"RemoteIP":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """"Protocol":"({protocol}[^"]+)"""",
      """LogonId":(null|({login_id}[^:]+?)),""",
      """InitiatingProcessFolderPath":"({process_path}[^"]+?)",""",
      """InitiatingProcessFileName":"({process_name}[^:]+?)",""",
      """InitiatingProcessCommandLine":"({process_command_line}[^<]+?)\s*","InitiatingProcess""",
      """InitiatingProcessId":({process_id}[^:]+?),""",
      """DeviceId":"({device_id}[^:]+?)",""",
      """InitiatingProcessMD5":"({hash_md5}[^:]+?)","""
    ]
    DupFields = ["host->dest_host"
}
```