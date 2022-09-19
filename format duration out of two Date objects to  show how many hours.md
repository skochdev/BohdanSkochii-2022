## format duration out of two Date objects to  show Hours

```js
import formatDistanceStrict from 'date-fns/formatDistanceStrict';  
  
// this function returns the estimated duration from start and end dates  
export function formatDuration(start, end) {  
  return formatDistanceStrict(Date.parse(start), Date.parse(end));  
}
```

Given start and end dates, function will return duration in hours 

Library used: ![[date formatting library date-fns]]