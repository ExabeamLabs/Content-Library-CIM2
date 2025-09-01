# Code Changes for dl-crowdstrike-falcon-app-activity-success-6 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'crowdstrike-falcon-sk4-app-activity-eventsimplename-1', 'crowdstrike-falcon-sk4-app-activity-eventsimplename') && !InList(toLower(event_code), 'regsystemconfigkeyupdate','injectedthread','wmicreateprocess') && !InList(toLower(os), 'mac', 'lin', 'win') |