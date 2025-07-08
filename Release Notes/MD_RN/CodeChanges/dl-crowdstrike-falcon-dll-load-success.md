# Code Changes for dl-crowdstrike-falcon-dll-load-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression | InList(type, 'crowdstrike-falcon-json-process-create-success-classifiedmoduleload') && !InList(toLower(os), 'win') | InList(type, 'crowdstrike-falcon-json-process-create-success-classifiedmoduleload', 'crowdstrike-falcon-json-dll-load-imagehash') && !InList(toLower(os), 'mac', 'lin', 'win') |