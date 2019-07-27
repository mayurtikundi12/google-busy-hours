node.js scraper for Google Places popular times data.

Installation
$ npm i busy-hours --save
Usage
Get your API key
Retrieve the Place ID
const busy_hours = require('busy-hours');

busy_hours(place_id, key).then(data => {
    do_something_with(data); 
 });
Response

{
    name: '...',
    formatted_address: '...',
    location: {
        lat: 52.225232,
        lng 21.0122137
    },
    week: [
    {
        day: 'Mon',
        hours: [ // or empty array
            { 
              hour: 6,
              percentage: 21,
            }, { 
              hour: 7,
              percentage: 37,
            } ...
        ]} ...
    ],
    now: { 
        hour: 12,
        percentage: 30,
      }
}

CAUTION!

Using this code may violate clause 10.1(b) of Google ToS, so beware.

No access to APIs or Content except through the Service. You will not access the Maps API(s) or the Content except through the Service. For example, you must not access map tiles or imagery through interfaces or channels (including undocumented Google interfaces) other than the Maps API(s).