#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-endpoint-login-success-4624"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch"
  Conditions = [
    """|Microsoft|Microsoft Windows|"""
    """|Microsoft-Windows-Security-Auditing:4624"""
  ]
  Fields = [
    """({event_name}An account was successfully logged on)"""
    """({event_code}4624)"""
    """\srt=({time}\d{13})"""
    """\sdntdom=({domain}[^\s]+)"""
    """\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
    """\sduid=({login_id}[^\s]+)"""
    """\scn1=({login_type}\d+)"""
    """\sdvchost=({host}[\w\-.]+)"""
    """\sdproc=(?:-|({process_path}[\w:\\.\-]+[\\]+({process_name}[^\\=]+?)?))\s\w+="""
    """Service_,ID=({user_sid}[^\s]+)\s"""
    """cs5=({auth_package}[^\s]+).+?cs5Label=Auth"""
    """\sdeviceProcessName =({auth_process}[^\s]+)"""
    """ src=(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+\w+="""
    """\sdst=(?:-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s+\w+="""
    """shost=({src_host}[^\s]+)"""
    """Key_,Length=({key_length}\d+)"""
    """\ssourceGeoLocationInfo=({location}[^=]+?)\s+\w+="""
  ]
  DupFields = [
    "host->dest_host"
  ]


}
```