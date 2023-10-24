#### Parser Content
```Java
{
Name = rsyslogdpstats-rp-kv-app-notification-success-imptcp
  Vendor = Unix
  Product = rsyslog
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """ rsyslogd-pstats """, """ origin=""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+[\+\-]\d+:\d+)\s+({host}[\w\-.]+)\s+rsyslogd-pstats""",
# closed is removed
# closetimeouts is removed
# decompressed is removed
# discarded is removed
# disk_usage_bytes is removed
    """\Wduration=({duration}.+?)\s+([\w\.]+=|$)""",
# enqueued is removed
# evicted is removed
# failed is removed
# full is removed
# inblock is removed
    """\Wlevel0=({level0}.+?)\s+([\w\.]+=|$)""",
# majflt is removed
# maxqsize is removed
# maxrss is removed
# maxused is removed
# minflt is removed
# missed is removed
# nf is removed
# nivcsw is removed
# numratelimiters is removed
# nvcsw is removed
# opened is removed
# openfailed is removed
# openfiles is removed
# origin is removed
# oublock is removed
# poll_failed is removed
# processed is removed
# ratelimit_discarded_in_interval is removed
# read is removed
# received is removed
# recovery_attempts is removed
# requests is removed
# resumed is removed
# rotations is removed
# size is removed
# stime is removed
# submitted is removed
# suspended is removed
# utime is removed
  ]


}
```