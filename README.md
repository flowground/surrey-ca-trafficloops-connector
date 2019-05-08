# ![LOGO](logo.png) City of Surrey Traffic Loop Count API. **flow**ground Connector

## Description

A generated **flow**ground connector for the City of Surrey Traffic Loop Count API. API (version 0.1).

Generated from: https://api.apis.guru/v2/specs/surrey.ca/trafficloops/0.1/swagger.json<br/>
Generated at: 2019-05-07T17:44:19+03:00

## API Description

This API provides locations of City of Surrey traffic loops and the corresponding traffic loop counts in 15 minute intervals. While the counts are broken up by 15 minute intervals, the data is currently loaded only once per day.  We are hoping to increase this frequency to at least once every hour. The LOOP_ID field is common to both datasets and can be used to cross-reference them.

## Authorization

This API does not require authorization.

## Actions

### Provides traffic loop counts for the input time interval. The LOOP_ID and DATETIME combinations are unique in the output. The output timestamp will contain the time zone offset, either -08 (PST) or -07 (PDT) depending on whether daylight savings time was observed at the output datetime. In order to work with local time you may omit the time zone offset from the input and truncate it from the output.

*Tags:* `counts`

#### Input Parameters
* `startdatetime` - _optional_ - Beginning of the required date/time range in ISO 8601. For example March 24 2016 at 1:00 PM Pacific Standard Time would be 2016-03-24T13:00:00-08.
* `enddatetime` - _optional_ - End of the required date/time range. For details see the startdatetime parameter.

### Provides all the traffic loops maintained by the City of Surrey in GeoJSON format. LANE_DIRECTION indicates the heading of the traffic (NB, SB, EB, WB). INTERSECTION_ID corresponds to the INTID field in the intersections dataset which can be found on the Surrey Open Data site. ROAD_FACILITYID indicates which road segment the loop is located on.  This corresponds to the FACILITYID in the Road Centrelines dataset on the City of Surrey Open Data site.

*Tags:* `loops`

#### Input Parameters
* `proj_epsg` - _optional_ - The output projection EPSG code.  Eg. WGS84 is 4326 and NAD 83 UTM Zone 10 is 26910.  If this is left blank, the default is 4326.  For more on EPSG codes please see http://spatialreference.org/

## License

**flow**ground :- Telekom iPaaS / surrey-ca-trafficloops-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
