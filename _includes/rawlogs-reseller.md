# Raw Logs API

## Get Raw Logs

Retrieve up to five days of raw log data

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients/{id}/v3/reporting/logs.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | ---
`start` | now() - 1 hour | ISO-8601 formatted date/time | The start of the range for requests to pull. |
`end` | now() | ISO-8601 formatted date/time | The end of the range for requests to pull |
`zones` | - | CSV of ints | The specific zones whose requests you want to pull. Separate multiple zone ids by comma |
`uri` | - | string | Use this filter to view requests made for a specific resource (or group of resources). You can do a literal match or regular expression in this field (i.e. '/images/header.png' or 'regex:/images/') |
`status` | - | CSV of ints | The specific HTTP status code responses you want to pull. Separate multiple HTTP status codes by comma (i.e. 200,201,304) |
`ssl` | both | enum(nossl, ssl, both) | Use this filter to distinguish between SSL and non-SSL traffic (choose nossl, ssl or both) |
`user_agent` | - | string | Filter logs by specific user agents. You can do a literal match or regular expression in this field (i.e. 'Python MaxCDN API Client' or 'regex:Chrome') |
`referer` | - | string | Filter logs by a specific referer. You can do a literal match or regular expression in this field (i.e. 'www.maxcdn.com' or 'regex:maxcdn.com') |
`pop` | - | CSV of strings  | Filter logs by specific POPs (Points Of Presence), use comma separation for multiple POPs. Possible values: ams, atl, aus, chi, dal, den, fra, hkg, jfk, lax, lhr, mia, sea, sfo, sin, sjc, slc, tko, vir |
`query_string` | - | string | Filter logs by a specific query string. You can do a literal match or regular expression in this field (i.e. 'width=600' or 'regex:width') |
`limit` | 100 | int | How many records should be retrieved per page. Maximum is 1000 |
`start_key` | - | string | String-based key for next page of records to return, for easy pagination or streaming. This key will be provided in the "next_page_key" from a response. |
`sort` | recent | enum(recent, oldest) | Display records sorted by newest first or oldest first |


### Response Parameters

Parameter | Description |
--- | --- | ---
`limit` | The maximum number of records retrieved |
`page` | The current page of records retrieved |
`request_time` | Time in milliseconds for request to complete |
`next_page_key` | Number string that can be used to load the next page |
`records` | Total records displayed |
`bytes` | Total bytes of request |
`client_asn` | Visitor's "access network" (ISP) |
`client_city` | Visitor's city |
`client_continent` | Visitor's continent |
`client_country` | Visitor's country |
`client_dma` | Visitor's "designated market area" |
`client_ip` | Visitor's public IP |
`client_latitude` | Visitor's geographical latitude (roughly) |
`client_longitude` | Visitor's geographical longitude (roughly) |
`client_state` | Visitor's state |
`company_id` | Your company ID |
`cache_status` | CDN status of the file (HIT, MISS) |
`hostname` | Domain name that was visited |
`method` | HTTP request method |
`origin_time` | How long it takes MaxCDN to retrieve the file (if cache status was a MISS) |
`pop` | Point Of Presence that was hit (LAX, LHR, TYO, etc.) |
`protocol` | HTTP protocol used |
`query_string` | Query string attached to a file (ex. ver=1.2) |
`referer` | Referring site |
`scheme` | HTTP or HTTPS |
`status` | HTTP status code (200, 404, 302, etc.) |
`time` | UTC timestamp of the request |
`uri` | File requested |
`user_agent` | Text identifying the visitor's browser |
`zone_id` | ID of the Push/Pull/VOD zone hit |

### Code Samples

<ul class="nav nav-tabs" id="myTab101">
  <li class="active"><a href="#ruby101" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python101" data-toggle='tab'>Python</a></li>
  <li><a href="#perl101" data-toggle='tab'>Perl</a></li>
  <li><a href="#php101" data-toggle='tab'>PHP</a></li>
  <li><a href="#node101" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp101" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#java101" data-toggle='tab'>Java</a></li>
  <li><a href="#response101" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby101">
<pre>
api.get('/clients/{id}/v3/reporting/logs.json?start=2014-01-30&end=2014-01-31&status=200')</pre>
  </div>
  <div class="tab-pane" id="python101">
<pre>
params = {"start":"2014-01-30", "end":"2014-01-31", "status":"200"}
api.get('/clients/{id}/v3/reporting/logs.json', data=params)</pre>
  </div>
  <div class="tab-pane" id="perl101">
<pre>
$api->get("/clients/{id}/v3/reporting/logs.json?start=2014-01-30&end=2014-01-31&status=200");</pre>
  </div>
  <div class="tab-pane" id="php101">
<pre>
$params = array("start"=>"2014-01-30", "end"=>"2014-01-31", "status"=>"200")
$api->get('/clients/{id}/v3/reporting/logs.json', $params)</pre>
  </div>
  <div class="tab-pane" id="node101">
<pre>
api.get('/clients/{id}/v3/reporting/logs.json?start=2014-01-30&end=2014-01-31&status=200', function(err, response) {
  console.log(response);
});</pre>
  </div>
  <div class="tab-pane" id="csharp101">
<pre>
api.Get("/clients/{id}/v3/reporting/logs.json?start=2014-01-30&end=2014-01-31&status=200");
</pre>
  </div>
 <div class="tab-pane" id="java101">
  <pre>
Console.log(api.get("/clients/{id}/v3/reporting/logs.json?start=2015-12-01&end=2015-12-02&status=200"));</pre>
    </div>
  <div class="tab-pane" id="response101">
    <pre>
{
  "limit":1000,
  "page":1,
  "total":3,
  "next_page_key":"1234abcdef",
  "records":[
    {
      "bytes":175953,
      "asn":"AS4804 Microplex PTY LTD",
      "city":"Brisbane",
      "continent":"OC",
      "country":"AU",
      "dma":"0",
      "ip":"127.0.0.1",
      "latitude":0,
      "longitude":1.2345,
      "cache_status":"HIT",
      "hostname":"cdn.example.com",
      "method":"GET",
      "origin_time":"0",
      "pop":"lax",
      "protocol":"HTTP/1.1",
      "query_string":"",
      "scheme":"https",
      "status_code":200,
      "request_time":"2014-01-30T17:00:12Z",
      "uri":"/content.png",
      "user_agent":"Opera/9.80 (Windows NT 5.1; Edition DriverPack) Presto/2.12.388 Version/12.16",
      "zone":"example"
    },
    {
      "bytes":175953,
      "asn":"AS4804 Microplex PTY LTD",
      "city":"Brisbane",
      "continent":"OC",
      "country":"AU",
      "dma":"0",
      "ip":"127.0.0.1",
      "latitude":0.0,
      "longitude":0.12345,
      "cache_status":"HIT",
      "hostname":"cdn.example.com",
      "method":"GET",
      "origin_time":"0",
      "pop":"lax",
      "protocol":"HTTP/1.1",
      "query_string":"ver=1.2",
      "scheme":"https",
      "status_code":200,
      "request_time":"2014-01-30T17:00:12Z",
      "uri":"/sample/test.swf",
      "user_agent":"Opera/9.80 (Windows NT 5.1; Edition DriverPack) Presto/2.12.388 Version/12.16",
      "zone":"example"
    }
  ]
}</pre>
  </div>
</div>
