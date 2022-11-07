#### Parser Content
```Java
{
Name = microsoft-exchange-cef-email-send-originating
Vendor = "Microsoft"
Product = "Microsoft Exchange"
TimeFormat = "epoch"
Conditions = [
  """|Microsoft|Exchange Server|"""
  """flexString1=Originating"""
]
Fields = [
  """\srt=({time}\d+)"""
  """\sdvc=({host}[\d.]+)"""
  """\sdvchost=({host}[^\s]*)"""
  """\scs6=({orig_user}.+?)\s+\w+="""
  """\ssuser=({email_address}.+?)\s+\w+="""
  """\sduser=({dest_email_address}[^\s@;,"]+@[^\s@;,"]+)"""
  """\sduser=({email_recipients}.+?)\s+\w+="""
  """\smsg=({email_subject}.+?)\s+\w+="""
  """\|RECEIVE\|RECEIVE\|.+?in=({bytes}\d+)"""
  """\|SEND\|SEND\|.+?out=({bytes}\d+)"""
  """\seventId=({alert_id}\d+)"""
  """\ssourceServiceName =({alert_name}[^\s]+)"""
  """\ssourceServiceName =({alert_type}[^\s]+)"""
  """CEF([^\|]*\|){6}({alert_severity}[^|]+)"""
  """CEF([^\|]*\|){5}({action}[^|]+)"""
  """({direction}o)"""
  """\scategoryOutcome=(\/)?({result}[^\s]*)"""
]
DupFields = [
  "orig_user->email_address"
  "orig_user->user"
]
ParserVersion = "v1.0.0"


}
```