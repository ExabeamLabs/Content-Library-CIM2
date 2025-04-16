#### Parser Content
```Java
{
Name = claroty-ctd-cef-app-activity-success-fschange
  ParserVersion = "v1.0.0"
  Conditions = [ """CEF:""", """|CTD|""", """|Fs Change|""", """|CtdSourceIp=""" ]
  Fields = ${ClarotyParserTemplates.claroty-schneider-events.Fields}[
    """({app}CTD)"""
  ]
  DupFields = ["event_name->operation"]

claroty-schneider-events {
    Vendor = Claroty
    Product = CTD
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Fields = [
      """CtdSourceIp=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s"""
      """CtdDestinationIp=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s"""
      """CtdSourceMac=({src_mac}[^\s]+)"""
      """CtdDestinationMac=({dest_mac}[^\s]+)"""
      """CtdSourceHost=({src_host}[\w.-]+)"""
      """CtdDestinationHost=({dest_host}[\w.-]+)"""
      """CtdTimeGenerated=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
      """CtdDeviceExternalId=({device_id}[^=]+)\s+\w+="""
      """CtdMessage=({additional_info}[^=]+)\s+\w+="""
      """CtdAlertLink=({url}[^\s]+)"""
      """CtdAlertScore=({severity}\d+)"""
      """CtdSignatureCriticality=({severity}[^=]+)\s+\w+="""
      """\|Schneider\|CTD\|([^\|]+\|){2}({event_name}[^\|]+)\|"""
      """CtdProtocol=({protocol}[^\s]+)"""
      """CtdMitreAttackTacticNames=({mitre_labels}[^=]+?)\s\w+="""
    
}
```