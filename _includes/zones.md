# Zones API

## List Zones

Returns a list of all zones on the specified account

<div class="heading">
	<div class="url GET">
		<span class="http_method">GET</span>
		<span class="path">https://rws.maxcdn.com/{companyalias}/zones.json</span>
	</div>
</div>

### Code Samples

<ul class="nav nav-tabs" id="myTab10">
	<li class="active"><a href="#ruby10" data-toggle='tab'>Ruby</a></li>
	<li><a href="#python10" data-toggle='tab'>Python</a></li>
	<li><a href="#perl10" data-toggle='tab'>Perl</a></li>
	<li><a href="#php10" data-toggle='tab'>PHP</a></li>
	<li><a href="#node10" data-toggle='tab'>Node</a></li>
	<li><a href="#csharp10" data-toggle='tab'>.NET/C#</a></li>
	<li><a href="#response10" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
	<div class="tab-pane active" id="ruby10">
    		<pre>
api.get('/zones.json')</pre>
	</div>

  <div class="tab-pane" id="python10">
    <pre>
api.get('/zones.json')</pre>

  </div>
    <div class="tab-pane" id="perl10">
    <pre>
$api->get("/zones.json");</pre>

  </div>
  <div class="tab-pane" id="php10">
    <pre>
$api->get('/zones.json');</pre>
  </div>
  <div class="tab-pane" id="node10">
  <pre>
api.get('/zones.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp10">
  <pre>
api.Get("/zones/pull.json");
</pre>
  </div>
  <div class="tab-pane" id="response10">
    <pre>
{
    "code": 200,
    "data": {
        "current_page_size": 2,
        "page": 1,
        "page_size": "50",
        "pages": 1,
        "total": 2,
        "zones": [
            {
                "cdn_url": "cdn.somedomain.com",
                "creation_date": "2013-05-15 20:45:44",
                "id": "#####",
                "inactive": "0",
                "label": "personal",
                "locked": "0",
                "name": "zoneName",
                "suspend": "0",
                "tmp_url": "zone.alias.netdna-cdn.com",
                "type": "2"
            }
        ]
    }
}</pre>
  </div>
</div>

## Get Zone Summary

Gets a summarized count of all zone types on the specified
account

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones.json/summary</span></div>
</div>


### Response Parameters

Parameter | Description |
--- | --- | ---
`pull` | The number of pull zones for your account |
`push` | The number of push zones for your account |
`vod` | The number of vod zones for your account |


### Code Samples

<ul class="nav nav-tabs" id="myTab11">
  <li class="active"><a href="#ruby11" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python11" data-toggle='tab'>Python</a></li>
  <li><a href="#perl11" data-toggle='tab'>Perl</a></li>
  <li><a href="#php11" data-toggle='tab'>PHP</a></li>
  <li><a href="#node11" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp11" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response11" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby11">
    <pre>
api.get('/zones.json/summary')</pre>
  </div>
  <div class="tab-pane" id="python11">
    <pre>
api.get('/zones.json/summary')</pre>
  </div>
    <div class="tab-pane" id="perl11">
    <pre>
$api->get("/zones.json/summary");</pre>
  </div>
  <div class="tab-pane" id="php11">
    <pre>
$api->get('/zones.json/summary');</pre>
  </div>
  <div class="tab-pane" id="node11">
  <pre>
api.get('/zones.json/summary', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp11">
  <pre>
api.Get("/zones.json/summary");
</pre>
  </div>
  <div class="tab-pane" id="response11">
    <pre>
{
    "code": 200,
    "data": {
        "summary": {
            "pull": 1,
            "push": 1,
            "vod": 1
        }
    }
}</pre>
  </div>
</div>

## Get Zone Count

Counts all zones on the specified account

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones.json/count</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`count` | The total number of content zones for your account |

### Code Samples

<ul class="nav nav-tabs" id="myTab12">
  <li class="active"><a href="#ruby12" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python12" data-toggle='tab'>Python</a></li>
  <li><a href="#perl12" data-toggle='tab'>Perl</a></li>
  <li><a href="#php12" data-toggle='tab'>PHP</a></li>
  <li><a href="#node12" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp12" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response12" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby12">
    <pre>
api.get('/zones.json/count')</pre>
  </div>
  <div class="tab-pane" id="python12">
    <pre>
api.get('/zones.json/count')</pre>
  </div>
    <div class="tab-pane" id="perl12">
    <pre>
$api->get("/zones.json/count");</pre>
  </div>
  <div class="tab-pane" id="php12">
    <pre>
$api->get('/zones.json/count');</pre>
  </div>
  <div class="tab-pane" id="node12">
  <pre>
api.get('/zones.json/count', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp12">
  <pre>
api.Get("/zones.json/count");
</pre>
  </div>
  <div class="tab-pane" id="response12">
    <pre>
{
  "code":200,"data":
    {
      "count":"4"
    }
}</pre>
  </div>
</div>

# Pull Zone API

## List Pull Zones

Returns a list of all pull zones on the specified account

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/pull.json</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | Pull Zone ID |
`name` | Pull Zone name |
`url` | Origin URL |
`port` | Port |
`ip` | IP address of the Origin URL |
`compress` | Enables on the fly GZip compression of your files from our edge servers for the following file types: text/plain, text/html, text/javascript, text/css, text/xml, application/javascript, application/x-javascript, application/xml, text/x-component, application/json, application/xhtml+xml, application/rss+xml, application/atom+xml, app/vnd.ms-fontobject, image/svg+xml, application/x-font-ttf, font/opentype, application/octet-stream |
`backend_compress` | Enables us to cache, from origin, GZip compressed versions of your files for the following file types: text/plain, text/html, text/javascript, text/css, text/xml, application/javascript, application/x-javascript, application/xml, text/x-component, application/json, application/xhtml+xml, application/rss+xml, application/atom+xml, app/vnd.ms-fontobject, image/svg+xml, application/x-font-ttf, font/opentype |
`queries` | Treat Query Strings as a separate cacheable item |
`set_host_header` | The URL sent as the Host in all HTTP Response Headers |
`cache_valid` | Ignore the origin Cache-Control Header and set every request to have a Max-Age of 1d, 7d, 1M or 12M |
`ignore_setcookie_header` | Ignore any cookies set by the origin in order to make the content consistently cacheable |
`ignore_cache_control` | Ignore any max age values set by the origin and use the CDN set value instead |
`use_stale` | Serve expired content while fetching new content. This will also cause the CDN to serve expired content in cases where the origin is down |
`proxy_cache_lock` | When multiple requests for an uncached file are received, they will wait until the first response is received rather than sending each request back to the origin |
`label` | Something that describes your zone |
`valid_referers` | List of domains for http referrer protection (separated by space), only the domains in the list will be treated as valid referrers |
`expires` | Set any request with a no "Cache-Control header" from the origin to stay on the server. Possible values are 1d, 7d, 1M, 12M |
`disallow_robots` | Enable robots.txt |
`disallow_robots_txt` | Use custom robots.txt |
`canonical_link_headers` | Pass the canonical URL in the Link HTTP Header |
`content_disposition` | Force files to download |
`pseudo_streaming` | Enable the zone for pseudo streaming content |
`sslshared` | Enable Shared SSL for your zone, so you can use HTTPS, using our SSL certificate for netdna-ssl.com |
`suspend` | Flag denoting if the zone has been suspended |
`locked` | Flag denoting if the zone has been locked |
`inactive` | Flag denoting if the zone has been deleted |
`creation_date` | Date Created |
`spdy` | Flag denoting if the zone has the SPDY protocol enabled |
`ssl` | Read-only flag denoting if the zone has Dedicated IP SSL enabled |
`ssl_sni` | Read-only flag denoting if the zone has SNI SSL enabled |
`geo_enabled` | Read-only flag denoting if the zone has 'More Locations' enabled |

### Code Samples

<ul class="nav nav-tabs" id="myTab13">
  <li class="active"><a href="#ruby13" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python13" data-toggle='tab'>Python</a></li>
  <li><a href="#perl13" data-toggle='tab'>Perl</a></li>
  <li><a href="#php13" data-toggle='tab'>PHP</a></li>
  <li><a href="#node13" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp13" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response13" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby13">
    <pre>
api.get('/zones/pull.json')</pre>
  </div>
  <div class="tab-pane" id="python13">
    <pre>
api.get('/zones/pull.json')</pre>
  </div>
    <div class="tab-pane" id="perl13">
    <pre>
$api->get("/zones/pull.json")</pre>
  </div>
  <div class="tab-pane" id="php13">
    <pre>
$api->get('/zones/pull.json');</pre>
  </div>
  <div class="tab-pane" id="node13">
  <pre>
api.get('/zones/pull.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp13">
  <pre>
api.Post("/zones/pull.json");
</pre>
  </div>
  <div class="tab-pane" id="response13">
    <pre>
{
    "code": 200,
    "data": {
        "current_page_size": 3,
        "page": 1,
        "page_size": "50",
        "pages": 1,
        "pullzones": [
            {
                "backend_compress": "0",
                "cache_valid": "1d",
                "canonical_link_headers": "0",
                "cdn_url": "cdn.somedomain.com",
                "compress": "1",
                "content_disposition": "0",
                "creation_date": "2013-05-15 20:45:44",
                "disallow_robots": "0",
                "disallow_robots_txt": null,
                "dns_check": "1",
                "expires": null,
                "hide_setcookie_header": "0",
                "id": "96061",
                "ignore_cache_control": "0",
                "ignore_setcookie_header": "0",
                "inactive": "0",
                "ip": "205.134.255.49",
                "label": "personal",
                "locked": "0",
                "name": "somedomain",
                "port": "80",
                "proxy_cache_lock": "0",
                "pseudo_streaming": "0",
                "queries": "1",
                "server_id": "18",
                "set_host_header": null,
                "sslshared": "0",
                "suspend": "0",
                "tmp_url": "somedomain.alias.netdna-cdn.com",
                "type": "2",
                "upstream_enabled": "0",
                "url": "http://somedomain.net",
                "use_stale": "0",
                "valid_referers": null,
                "spdy": 1,
                "ssl": 1,
                "ssl_sni": 0,
                "geo_enabled": 1
            },
            <...>,
            {
                "backend_compress": "0",
                "cache_valid": "1d",
                "canonical_link_headers": "0",
                "cdn_url": "newpullzone3.alias.netdna-cdn.com",
                "compress": "0",
                "content_disposition": "0",
                "creation_date": "2013-05-24 16:18:19",
                "disallow_robots": "0",
                "disallow_robots_txt": null,
                "dns_check": "1",
                "expires": null,
                "hide_setcookie_header": "0",
                "id": "97312",
                "ignore_cache_control": "0",
                "ignore_setcookie_header": "0",
                "inactive": "0",
                "ip": "205.134.255.49",
                "label": null,
                "locked": "0",
                "name": "newpullzone3",
                "port": "80",
                "proxy_cache_lock": "0",
                "pseudo_streaming": "0",
                "queries": "1",
                "server_id": "18",
                "set_host_header": null,
                "sslshared": "0",
                "suspend": "0",
                "tmp_url": "newpullzone3.alias.netdna-cdn.com",
                "type": "2",
                "upstream_enabled": "0",
                "url": "http://somedomain.net",
                "use_stale": "0",
                "valid_referers": null,
                "spdy": 1,
                "ssl": 0,
                "ssl_sni": 1,
                "geo_enabled": 0
            }
        ],
        "total": 3
    }
}</pre>
  </div>
</div>

## Create Pull Zone

Creates a new pull zone

<div class="heading">
<div class="url POST"><span class="http_method">POST</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/pull.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`name` | - | <span class="label important">required</span><br />length: 3-32 chars; only letters, digits, and dash (-)accepted | Pull Zone Name |
`url` | - | <span class="label important">required</span><br />length: 4-100 chars; only valid URLs accepted | Origin URL |
`port` | 80 | length: 1-5 chars; only digits accepted | Port |
`dns_check` | 1 | only 0 or 1 accepted | This field determines how your Origin resolves. When set to 1, we automatically grab the origin's IP using DNS. Setting it to 0 allows you explicitly provide the IP of the origin. |
`ip` | - | length: 1-10 chars, only digits accepted | Valid IP address of the Origin URL. Be sure to set `dns_check` to 0 to prevent this value from being overwritten. |
`compress` | 0 | only 0 or 1 accepted | Enables on the fly GZip compression of your files from our edge servers for the following file types: text/plain, text/html, text/javascript, text/css, text/xml, application/javascript, application/x-javascript, application/xml, text/x-component, application/json, application/xhtml+xml, application/rss+xml, application/atom+xml, app/vnd.ms-fontobject, image/svg+xml, application/x-font-ttf, font/opentype |
`backend_compress` | 0 | only 0 or 1 accepted | Enables us to cache, from origin, GZip compressed versions of your files for the following file types: text/plain, text/html, text/javascript, text/css, text/xml, application/javascript, application/x-javascript, application/xml, text/x-component, application/json, application/xhtml+xml, application/rss+xml, application/atom+xml, app/vnd.ms-fontobject, image/svg+xml, application/x-font-ttf, font/opentype |
`queries` | 0 | only 0 or 1 accepted | Treat Query Strings as a separate cacheable item |
`set_host_header` | - | length: 4-100 chars; only valid URLs accepted | The URL to send as the Host in all HTTP Response Headers |
`cache_valid` | 1d | length: 1-30 chars; must be a number followed by one of s, m, h, d, M, or Y | Ignore the origin Cache-Control Header and set every request to have a Max-Age of 1d, 7d, 1M or 12M |
`ignore_setcookie_header` | 0 | only 0 or 1 accepted | Ignore any cookies set by the origin in order to make the content consistently cacheable |
`ignore_cache_control` | 0 | only 0 or 1 accepted | Ignore any max age values set by the origin and use the CDN set value instead |
`use_stale` | 0 | List of status codes separated with space - empty character - (?use_stale=500 502 503 504 403 404) are accepted as a valid request. 0 or 1 are accepted by legacy but, these are not valid parameters any more. To disable use_stale you can pass 0 (as a part of the legacy) or empty string "".| Serve expired content while fetching new content. This will also cause the CDN to serve expired content in cases where the origin is down |
`proxy_cache_lock` | 0 | only 0 or 1 accepted | When multiple requests for an uncached file are received, they will wait until the first response is received rather than sending each request back to the origin |
`label` | - | length: 1-255 chars | Something that describes your zone |
`valid_referers` | - | length: 1-100 chars | List of domains for http referrer protection (separated by space), only the domains in the list will be treated as valid referrers |
`expires` | 1d | length: 1-32 chars | Set any request with a no "Cache-Control header" from the origin to stay on the server. Possible values are 1d, 7d, 1M, 12M |
`disallow_robots` | 0 | only 0 or 1 accepted | Enable robots.txt |
`disallow_robots_txt` | - | length 1-255 chars | Use custom robots.txt |
`canonical_link_headers` | 1 | only 0 or 1 accepted | Pass the canonical URL in the Link HTTP Header |
`content_disposition` | 0 | only 0 or 1 accepted | Force files to download |
`x_forward_for` | 0 | only 0 or 1 accepted | Add X-Forwarded-For (XFF) HTTP Header |
`pseudo_streaming` | 0 | only 0 or 1 accepted | Enable the zone for pseudo streaming content |
`secret` | - | length: 1 - 32 chars | Use a secret to protect your files from unwanted visitors |
`sslshared` | 0 | only 0 or 1 accepted | Enable Shared SSL for your zone, so you can use HTTPS, using our SSL certificate for netdna-ssl.com |
`spdy` | 0 | only 0 or 1 accepted | Enable SPDY protocol on the zone (requires SSL) |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | Pull Zone ID |
`name` | Pull Zone name |
`url` | Origin URL |
`port` | Port |
`ip` | IP address of the Origin URL |
`compress` | Enables on the fly GZip compression of your files from our edge servers for the following file types: text/plain, text/html, text/javascript, text/css, text/xml, application/javascript, application/x-javascript, application/xml, text/x-component, application/json, application/xhtml+xml, application/rss+xml, application/atom+xml, app/vnd.ms-fontobject, image/svg+xml, application/x-font-ttf, font/opentype |
`backend_compress` | Enables us to cache, from origin, GZip compressed versions of your files for the following file types: text/plain, text/html, text/javascript, text/css, text/xml, application/javascript, application/x-javascript, application/xml, text/x-component, application/json, application/xhtml+xml, application/rss+xml, application/atom+xml, app/vnd.ms-fontobject, image/svg+xml, application/x-font-ttf, font/opentype |
`queries` | Treat Query Strings as a separate cacheable item |
`set_host_header` | The URL sent as the Host in all HTTP Response Headers |
`cache_valid` | Ignore the origin Cache-Control Header and set every request to have a Max-Age of 1d, 7d, 1M or 12M |
`ignore_setcookie_header` | Ignore any cookies set by the origin in order to make the content consistently cacheable |
`ignore_cache_control` | Ignore any max age values set by the origin and use the CDN set value instead |
`use_stale` | Serve expired content while fetching new content. This will also cause the CDN to serve expired content in cases where the origin is down |
`proxy_cache_lock` | When multiple requests for an uncached file are received, they will wait until the first response is received rather than sending each request back to the origin |
`label` | Something that describes your zone |
`valid_referers` | List of domains for http referrer protection (separated by space), only the domains in the list will be treated as valid referrers |
`expires` | Set any request with a no "Cache-Control header" from the origin to stay on the server. Possible values are 1d, 7d, 1M, 12M |
`disallow_robots` | Enable robots.txt |
`disallow_robots_txt` | Use custom robots.txt |
`canonical_link_headers` | Pass the canonical URL in the Link HTTP Header |
`content_disposition` | Force files to download |
`x_forward_for` | Add X-Forwarded-For (XFF) HTTP Header |
`pseudo_streaming` | Enable the zone for pseudo streaming content |
`sslshared` | Enable Shared SSL for your zone, so you can use HTTPS, using our SSL certificate for netdna-ssl.com |
`suspend` | Flag denoting if the zone has been suspended |
`locked` | Flag denoting if the zone has been locked |
`inactive` | Flag denoting if the zone has been deleted |
`creation_date` | Date Created |
`spdy` | Flag denoting if the zone has the SPDY protocol enabled |
`ssl` | Read-only flag denoting if the zone has Dedicated IP SSL enabled |
`ssl_sni` | Read-only flag denoting if the zone has SNI SSL enabled |
`geo_enabled` | Read-only flag denoting if the zone has 'More Locations' enabled |

### Code Samples

<ul class="nav nav-tabs" id="myTab14">
  <li class="active"><a href="#ruby14" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python14" data-toggle='tab'>Python</a></li>
  <li><a href="#perl14" data-toggle='tab'>Perl</a></li>
  <li><a href="#php14" data-toggle='tab'>PHP</a></li>
  <li><a href="#node14" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp14" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response14" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby14">
    <pre>
params = {"name"=>"newPullZone6","url"=>"http://somedomain.com"}
api.post('/zones/pull.json',params)</pre>
  </div>
  <div class="tab-pane" id="python14">
    <pre>
params = {"name":"newPullZone5","url":"http://somedomain.net"}
api.post('/zones/pull.json',data=params)</pre>
  </div>
    <div class="tab-pane" id="perl14">
    <pre>
my @params = {name => 'perltest5', url => 'http://www.domain.com'};
$api->post("/zones/pull.json", @params);</pre>
  </div>
  <div class="tab-pane" id="php14">
    <pre>
$params =  array("name"=>"newPullZone2","url"=>"http://somedomain.net");
$api->post('/zones/pull.json',$params);</pre>
  </div>
  <div class="tab-pane" id="node14">
  <pre>
api.post('/zones/pull.json', { name: 'newPullZone2', url: 'http://somedomain.net' }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp14">
  <pre>
Console.Write("Zone Name: \n");
string ZoneName = Console.ReadLine();
Console.Write("Origin URL (starting with http://): \n");
string url = Console.ReadLine();

api.Post("/zones/pull.json", "url=" + url + "&name=" + ZoneName);
</pre>
  </div>
  <div class="tab-pane" id="response14">
    <pre>
{
    "code": 201,
    "data": {
        "pullzone": {
            "backend_compress": 0,
            "cache_valid": "1d",
            "canonical_link_headers": 1,
            "cdn_url": "newpullzone3.alias.netdna-cdn.com",
            "compress": 0,
            "content_disposition": 0,
            "creation_date": "2013-05-24 16:18:19",
            "disallow_robots": 0,
            "disallow_robots_txt": null,
            "dns_check": 0,
            "expires": null,
            "hide_setcookie_header": 0,
            "id": 97312,
            "ignore_cache_control": 0,
            "ignore_setcookie_header": 0,
            "inactive": 0,
            "ip": "205.134.255.49",
            "label": null,
            "locked": 0,
            "name": "newpullzone3",
            "port": 80,
            "proxy_cache_lock": 0,
            "pseudo_streaming": 0,
            "queries": "1",
            "server_id": "18",
            "set_host_header": 1,
            "sslshared": null,
            "suspend": 0,
            "tmp_url": "newpullzone3.alias.netdna-cdn.com",
            "type": 2,
            "upstream_enabled": 0,
            "url": "http://somedomain.net",
            "use_stale": 0,
            "x_forward_for": 0,
            "valid_referers": null,
            "spdy": 1,
            "ssl": 1,
            "ssl_sni": 0,
            "geo_enabled": 1
        }
    }
}</pre>
  </div>
</div>

## Get Pull Zones Count

Counts all pull zones on the specified account

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/pull.json/count</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`count` | The number of pull zones on the specified account |

### Code Samples

<ul class="nav nav-tabs" id="myTab15">
  <li class="active"><a href="#ruby15" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python15" data-toggle='tab'>Python</a></li>
  <li><a href="#perl15" data-toggle='tab'>Perl</a></li>
  <li><a href="#php15" data-toggle='tab'>PHP</a></li>
  <li><a href="#node15" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp15" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response15" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby15">
    <pre>
api.get('/zones/pull.json/count')</pre>
  </div>
  <div class="tab-pane" id="python15">
    <pre>
api.get('/zones/pull.json/count')</pre>
  </div>
    <div class="tab-pane" id="perl15">
    <pre>
$api->get("/zones/pull.json/count")</pre>
  </div>
  <div class="tab-pane" id="php15">
    <pre>
$api->get('/zones/pull.json/count');</pre>
  </div>
  <div class="tab-pane" id="node15">
  <pre>
api.get('/zones/pull.json/count', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp15">
  <pre>
api.Get("/zones/pull.json/count");
</pre>
  </div>
  <div class="tab-pane" id="response15">
    <pre>
{
  "code":200,"data":
    {
      "count": "3"
    }
}</pre>
  </div>
</div>

## Get Pull Zone

Gets a pull zone specified by the {zone_id} parameter

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/pull.json/{zone_id}</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The Pull Zone ID |
`name` | Pull Zone name |
`url` | Origin URL |
`port` | Port |
`ip` | Valid IP address of the Origin URL, if omitted the service will automatically try to find the IP |
`compress` | Enables on the fly GZip compression of your files from our edge servers for the following file types: text/plain, text/html, text/javascript, text/css, text/xml, application/javascript, application/x-javascript, application/xml, text/x-component, application/json, application/xhtml+xml, application/rss+xml, application/atom+xml, app/vnd.ms-fontobject, image/svg+xml, application/x-font-ttf, font/opentype |
`backend_compress` | Enables us to cache, from origin, GZip compressed versions of your files for the following file types: text/plain, text/html, text/javascript, text/css, text/xml, application/javascript, application/x-javascript, application/xml, text/x-component, application/json, application/xhtml+xml, application/rss+xml, application/atom+xml, app/vnd.ms-fontobject, image/svg+xml, application/x-font-ttf, font/opentype |
`queries` | Treat Query Strings as a separate cacheable item |
`set_host_header` | The URL sent as the Host in all HTTP Response Headers |
`cache_valid` | Ignore the origin Cache-Control Header and set every request to have a Max-Age of 1d, 7d, 1M or 12M |
`ignore_setcookie_header` | Ignore any cookies set by the origin in order to make the content consistently cacheable |
`ignore_cache_control` | Ignore any max age values set by the origin and use the CDN set value instead |
`use_stale` | Serve expired content while fetching new content. This will also cause the CDN to serve expired content in cases where the origin is down |
`proxy_cache_lock` | When multiple requests for an uncached file are received, they will wait until the first response is received rather than sending each request back to the origin |
`label` | Something that describes your zone |
`valid_referers` | List of domains for http referrer protection (separated by space), only the domains in the list will be treated as valid referrers |
`expires` | Set any request with a no "Cache-Control header" from the origin to stay on the server. Possible values are 1d, 7d, 1M, 12M |
`disallow_robots` | Enable robots.txt |
`disallow_robots_txt` | Use custom robots.txt |
`canonical_link_headers` | Pass the canonical URL in the Link HTTP Header |
`content_disposition` | Force files to download |
`x_forward_for` | Add X-Forwarded-For (XFF) HTTP Header |
`pseudo_streaming` | Enable the zone for pseudo streaming content |
`sslshared` | Enable Shared SSL for your zone, so you can use HTTPS, using our SSL certificate for netdna-ssl.com |
`suspend` | Flag denoting if the zone has been suspended |
`locked` | Flag denoting if the zone has been locked |
`inactive` | Flag denoting if the zone has been deleted |
`creation_date` | Date Created |
`spdy` | Flag denoting if the zone has the SPDY protocol enabled |
`ssl` | Read-only flag denoting if the zone has Dedicated IP SSL enabled |
`ssl_sni` | Read-only flag denoting if the zone has SNI SSL enabled |
`geo_enabled` | Read-only flag denoting if the zone has 'More Locations' enabled |

### Code Samples

<ul class="nav nav-tabs" id="myTab16">
  <li class="active"><a href="#ruby16" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python16" data-toggle='tab'>Python</a></li>
  <li><a href="#perl16" data-toggle='tab'>Perl</a></li>
  <li><a href="#php16" data-toggle='tab'>PHP</a></li>
  <li><a href="#node16" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp16" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response16" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby16">
    <pre>
id = '97167'
api.get('/zones/pull.json/'+id)</pre>
  </div>
  <div class="tab-pane" id="python16">
    <pre>
id = '97167'
api.get('/zones/pull.json/'+id)</pre>
  </div>
    <div class="tab-pane" id="perl16">
    <pre>
my $id = 96076;
$api->get("/zones/pull.json/" . $id);</pre>
  </div>
  <div class="tab-pane" id="php16">
    <pre>
$id = '96076';
$api->get('/zones/pull.json/'.$id);</pre>
 </div>
  <div class="tab-pane" id="node16">
  <pre>
var id = '96076'
api.get('/zones/pull.json' + id, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp16">
  <pre>
Console.Write("Zone id: \n");
int id = Convert.ToInt32(Console.ReadLine());

api.Get("/zones/pull.json/" + id);
</pre>
  </div>
  <div class="tab-pane" id="response16">
    <pre>
{
    "code": 200,
    "data": {
        "pullzone": {
            "backend_compress": "0",
            "cache_valid": "1d",
            "canonical_link_headers": "0",
            "cdn_url": "cdn.somenewdomain.com",
            "compress": "0",
            "content_disposition": "0",
            "creation_date": "2013-05-23 19:38:30",
            "disallow_robots": "0",
            "disallow_robots_txt": null,
            "dns_check": "1",
            "expires": null,
            "hide_setcookie_header": "0",
            "id": "97167",
            "ignore_cache_control": "0",
            "ignore_setcookie_header": "0",
            "inactive": "0",
            "ip": "205.134.255.49",
            "label": "Some other description",
            "locked": "0",
            "name": "newpullzone2",
            "port": "80",
            "proxy_cache_lock": "0",
            "pseudo_streaming": "0",
            "queries": "1",
            "server_id": "18",
            "set_host_header": null,
            "sslshared": "0",
            "suspend": "0",
            "tmp_url": "newpullzone2.alias.netdna-cdn.com",
            "type": "2",
            "upstream_enabled": "0",
            "url": "http://somedomain.net",
            "use_stale": "0",
            "x_forward_for": "0",
            "valid_referers": null,
            "spdy": 1,
            "ssl": 1,
            "ssl_sni": 0,
            "geo_enabled": 1
        }
    }
}</pre>
  </div>
</div>

## Update Pull Zone

Updates a pull zone specified by the {zone_id} parameter

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/pull.json/{zone_id}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`url` | - | length: 4-100 chars; only valid URLs accepted | Origin URL |
`port` | 80 | length: 1-5 chars; only digits accepted | Port |
`dns_check` | 1 | only 0 or 1 accepted | This field determines how your Origin resolves. When set to 1, we automatically grab the origin's IP using DNS. Setting it to 0 allows you explicitly provide the IP of the origin. |
`ip` | - | length: 1-10 chars, only digits accepted | Valid IP address of the Origin URL. Be sure to set `dns_check` to 0 to prevent this value from being overwritten. |
`compress` | 0 | only 0 or 1 accepted | On the fly compression of your files served from our edges. Enables GZip compression for the following file types: text/plain, text/html, text/javascript, text/css, text/xml, application/javascript, application/x-javascript, application/xml, text/x-component, application/json, application/xhtml+xml, application/rss+xml, application/atom+xml, app/vnd.ms-fontobject, image/svg+xml, application/x-font-ttf, font/opentype |
`backend_compress` | 0 | only 0 or 1 accepted | Allow us to cache compressed versions of your files from the origin. Enables GZip compression for the following file types: text/plain, text/html, text/javascript, text/css, text/xml, application/javascript, application/x-javascript, application/xml, text/x-component, application/json, application/xhtml+xml, application/rss+xml, application/atom+xml, app/vnd.ms-fontobject, image/svg+xml, application/x-font-ttf, font/opentype |
`queries` | 0 | only 0 or 1 accepted | Treat Query Strings as a separate cacheable item |
`set_host_header` | - | length: 4-100 chars; only valid URLs accepted | The URL to send as the Host in all HTTP Response Headers |
`cache_valid` | - | length: 1-30 chars; must be a number followed by one of s, m, h, d, M, or Y | Ignore the origin Cache-Control Header and set every request to have a Max-Age of 1d, 7d, 1M or 12M |
`ignore_setcookie_header` | 0 | only 0 or 1 accepted | Ignore any cookies set by the origin in order to make the content consistently cacheable |
`ignore_cache_control` | 0 | only 0 or 1 accepted | Ignore any max age values set by the origin and use the CDN set value instead |
`use_stale` | 0 | List of status codes separated with space - empty character - (?use_stale=500 502 503 504 403 404) are accepted as a valid request. 0 or 1 are accepted by legacy but, these are not valid parameters any more. To disable use_stale you can pass 0 (as a part of the legacy) or empty string "". | Serve expired content while fetching new content. This will also cause the CDN to serve expired content in cases where the origin is down |
`proxy_cache_lock` | 0 | only 0 or 1 accepted | When multiple requests for an uncached file are received, they will wait until the first response is received rather than sending each request back to the origin |
`label` | - | length: 1-255 chars | Something that describes your zone |
`valid_referers` | - | length: 1-100 chars | List of domains for http referrer protection (separated by space), only the domains in the list will be treated as valid referrers |
`expires` | 1d | length: 1-32 chars | Set any request with a no "Cache-Control header" from the origin to stay on the server. Possible values are 1d, 7d, 1M, 12M |
`disallow_robots` | 0 | only 0 or 1 accepted | Enable robots.txt |
`disallow_robots_txt` | - | length: 1-255 chars | Use custom robots.txt |
`canonical_link_headers` | 1 | only 0 or 1 accepted | Pass the canonical URL in the Link HTTP Header |
`content_disposition` | 0 | only 0 or 1 accepted | Force files to download |
`x_forward_for` | 0 | only 0 or 1 accepted | Add X-Forwarded-For (XFF) HTTP Header |
`pseudo_streaming` | 0 | only 0 or 1 accepted | Enable the zone for pseudo streaming content |
`secret` | - | length: 1 - 32 chars | Use a secret to protect your files from unwanted visitors |
`sslshared` | 0 | only 0 or 1 accepted | Enable Shared SSL for your zone, so you can use HTTPS, using our SSL certificate for netdna-ssl.com |
`spdy` | 0 | only 0 or 1 accepted | Enable SPDY protocol on the zone (requires SSL) |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | Pull Zone ID |
`name` | Pull Zone name |
`url` | Origin URL |
`port` | Port |
`ip` | Valid IP address of the Origin URL, if omitted the service will automatically try to find the IP |
`compress` | On the fly compression of your files served from our edges. Enables GZip compression for the following file types: text/plain, text/html, text/javascript, text/css, text/xml, application/javascript, application/x-javascript, application/xml, text/x-component, application/json, application/xhtml+xml, application/rss+xml, application/atom+xml, app/vnd.ms-fontobject, image/svg+xml, application/x-font-ttf, font/opentype |
`backend_compress` | Allow us to cache compressed versions of your files from the origin. Enables GZip compression for the following file types: text/plain, text/html, text/javascript, text/css, text/xml, application/javascript, application/x-javascript, application/xml, text/x-component, application/json, application/xhtml+xml, application/rss+xml, application/atom+xml, app/vnd.ms-fontobject, image/svg+xml, application/x-font-ttf, font/opentype |
`queries` | Treat Query Strings as a separate cacheable item |
`set_host_header` | The URL sent as the Host in all HTTP Response Headers |
`cache_valid` | Ignore the origin Cache-Control Header and set every request to have a Max-Age of 1d, 7d, 1M or 12M |
`ignore_setcookie_header` | Ignore any cookies set by the origin in order to make the content consistently cacheable |
`ignore_cache_control` | Ignore any max age values set by the origin and use the CDN set value instead |
`use_stale` | Serve expired content while fetching new content. This will also cause the CDN to serve expired content in cases where the origin is down |
`proxy_cache_lock` | When multiple requests for an uncached file are received, they will wait until the first response is received rather than sending each request back to the origin |
`label` | Something that describes your zone |
`valid_referers` | List of domains for http referrer protection (separated by space), only the domains in the list will be treated as valid referrers |
`expires` | Set any request with a no "Cache-Control header" from the origin to stay on the server. Possible values are 1d, 7d, 1M, 12M |
`disallow_robots` | Enable robots.txt |
`disallow_robots_txt` | Use custom robots.txt |
`canonical_link_headers` | Pass the canonical URL in the Link HTTP Header |
`content_disposition` | Force files to download |
`x_forward_for` | Add X-Forwarded-For (XFF) HTTP Header |
`pseudo_streaming` | Enable the zone for pseudo streaming content |
`sslshared` | Enable Shared SSL for your zone, so you can use HTTPS, using our SSL certificate for netdna-ssl.com |
`suspend` | Flag denoting if the zone has been suspended |
`locked` | Flag denoting if the zone has been locked |
`inactive` | Flag denoting if the zone has been deleted |
`creation_date` | Date Created |
`spdy` | Flag denoting if the zone has the SPDY protocol enabled |
`ssl` | Read-only flag denoting if the zone has Dedicated IP SSL enabled |
`ssl_sni` | Read-only flag denoting if the zone has SNI SSL enabled |
`geo_enabled` | Read-only flag denoting if the zone has 'More Locations' enabled |

### Code Samples

<ul class="nav nav-tabs" id="myTab17">
  <li class="active"><a href="#ruby17" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python17" data-toggle='tab'>Python</a></li>
  <li><a href="#perl17" data-toggle='tab'>Perl</a></li>
  <li><a href="#php17" data-toggle='tab'>PHP</a></li>
  <li><a href="#node17" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp17" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response17" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby17">
    <pre>
id = '97167'
params = {"label"=>"Some other description"}
api.put('/zones/pull.json/'+id,params)</pre>

  </div>
  <div class="tab-pane" id="python17">
    <pre>
id = '97167'
params = {"label":"Some other description"}
api.put('/zones/pull.json/'+id,params=params)</pre>
  </div>
    <div class="tab-pane" id="perl17">
    <pre>
my $id = 236828;
my @params = ('compress=0');
$api->put("/zones/pull.json/" . $id, @params);</pre>
  </div>
  <div class="tab-pane" id="php17">
    <pre>
$id = '96167';
$params = array("label"=>"Some other description");
$api->put('/zones/pull.json/'.$id, $params);</pre>
  </div>
  <div class="tab-pane" id="node17">
  <pre>
var id = '96167'
api.put('/zones/pull.json' + id, { label: 'Some other description' }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp17">
  <pre>
Console.Write("Zone id to edit: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Property to edit/change (url/compression...): \n");
string prop = Console.ReadLine();
Console.Write("New value: \n");
string val = Console.ReadLine();

api.Put("/zones/pull.json/" + zoneID, prop + "=" + val);
</pre>
  </div>
  <div class="tab-pane" id="response17">
    <pre>
{
    "code": 200,
    "data": {
        "pullzone": {
            "backend_compress": "0",
            "cache_valid": "1d",
            "canonical_link_headers": "0",
            "cdn_url": "cdn.somenewdomain.com",
            "compress": "0",
            "content_disposition": "0",
            "creation_date": "2013-05-23 19:38:30",
            "disallow_robots": "0",
            "disallow_robots_txt": null,
            "dns_check": "1",
            "expires": null,
            "hide_setcookie_header": "0",
            "id": "97167",
            "ignore_cache_control": "0",
            "ignore_setcookie_header": "0",
            "inactive": "0",
            "ip": "205.134.255.49",
            "label": "Some other description",
            "locked": "0",
            "name": "newpullzone2",
            "port": "80",
            "proxy_cache_lock": "0",
            "pseudo_streaming": "0",
            "queries": "1",
            "server_id": "18",
            "set_host_header": null,
            "sslshared": "0",
            "suspend": "0",
            "tmp_url": "newpullzone2.alias.netdna-cdn.com",
            "type": "2",
            "upstream_enabled": "0",
            "url": "http://somedomain.net",
            "use_stale": "0",
            "x_forward_for": "0",
            "valid_referers": null,
            "spdy": 1,
            "ssl": 1,
            "ssl_sni": 0,
            "geo_enabled": 1
        }
    }
}</pre>
  </div>
</div>

## Enable Flex

Enables additional locations on a pull zone specified by the {zone_id} parameter

<div class="heading">
<div class="url POST"><span class="http_method">POST</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/pull/{zone_id}/flex.json</span></div>
</div>


### Code Samples

<ul class="nav nav-tabs" id="myTab17-1">
  <li class="active"><a href="#ruby17-1" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python17-1" data-toggle='tab'>Python</a></li>
  <li><a href="#perl17-1" data-toggle='tab'>Perl</a></li>
  <li><a href="#php17-1" data-toggle='tab'>PHP</a></li>
  <li><a href="#node17-1" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp17-1" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response17-1" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby17-1">
    <pre>
id = '97167'
api.post('/zones/pull/'+id+'/flex.json')</pre>
  </div>
  <div class="tab-pane" id="python17-1">
    <pre>
id = '97167'
api.post('/zones/pull/'+id+'/flex.json')</pre>
  </div>
    <div class="tab-pane" id="perl17-1">
    <pre>
my $id = 134458;
$api->post("/zones/pull/" . $id . "/flex.json");</pre>
  </div>
  <div class="tab-pane" id="php17-1">
    <pre>
$id = '97167';
$api->post('/zones/pull/'.$id.'/flex.json');</pre>
  </div>
  <div class="tab-pane" id="node17-1">
  <pre>
var id = '97167'
api.post('/zones/pull/' + id + '/flex.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp17-1">
  <pre>
Console.Write("Zone id to enable: \n");
int id = Convert.ToInt32(Console.ReadLine());

api.Post("/zones/pull/" + id + "/flex.json");
</pre>
  </div>
  <div class="tab-pane" id="response17-1">
    <pre>
{
  "code":200
}
</pre>
  </div>
</div>

## Disable Flex

Disables additional locations on a pull zone specified by the {zone_id} parameter

<div class="heading">
<div class="url DELETE"><span class="http_method">DELETE</span>
<span class="path"> https://rws.maxcdn.com/{companyalias}/zones/pull/{zone_id}/flex.json</span></div>
</div>


### Code Samples

<ul class="nav nav-tabs" id="myTab17-2">
  <li class="active"><a href="#ruby17-2" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python17-2" data-toggle='tab'>Python</a></li>
  <li><a href="#perl17-2" data-toggle='tab'>Perl</a></li>
  <li><a href="#php17-2" data-toggle='tab'>PHP</a></li>
  <li><a href="#node17-2" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp17-2" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response17-2" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby17-2">
    <pre>
id = '97167'
api.delete('/zones/pull/'+id+'/flex.json')</pre>
  </div>
  <div class="tab-pane" id="python17-2">
    <pre>
id = '97167'
api.delete('/zones/pull/'+id+'/flex.json')</pre>
  </div>
    <div class="tab-pane" id="perl17-2">
    <pre>
my $id = 134458;
$api->delete("/zones/pull/" . $id . "/flex.json");</pre>
  </div>
  <div class="tab-pane" id="php17-2">
    <pre>
$id = '97167';
$api->delete('/zones/pull'.$id.'flex.json);</pre>
  </div>
  <div class="tab-pane" id="node17-2">
  <pre>
var id = '97167'
api.delete('/zones/pull' + id + 'flex.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp17-2">
  <pre>
Console.Write("Zone id to disable: \n");
int id = Convert.ToInt32(Console.ReadLine());

api.Delete("/zones/pull/" + id + "/flex.json");
</pre>
  </div>
  <div class="tab-pane" id="response17-2">
    <pre>
{
  "code":200
}</pre>
  </div>
</div>

## Delete Pull Zone

Deletes a pull zone specified by the {zone_id} parameter

<div class="heading">
<div class="url DELETE"><span class="http_method">DELETE</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/pull.json/{zone_id}</span></div>
</div>


### Code Samples

<ul class="nav nav-tabs" id="myTab18">
  <li class="active"><a href="#ruby18" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python18" data-toggle='tab'>Python</a></li>
  <li><a href="#perl18" data-toggle='tab'>Perl</a></li>
  <li><a href="#php18" data-toggle='tab'>PHP</a></li>
  <li><a href="#node18" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp18" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response18" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby18">
    <pre>
id = '97167'
api.delete('/zones/pull.json/'+id)</pre>
  </div>
  <div class="tab-pane" id="python18">
    <pre>
id = '97167'
api.delete('/zones/pull.json/'+id)</pre>
  </div>
    <div class="tab-pane" id="perl18">
    <pre>
my $id = 236828;
$api->delete("/zones/pull.json/" . $id);</pre>
  </div>
  <div class="tab-pane" id="php18">
    <pre>
$id = '97167';
$api->delete('/zones/pull.json/'.$id);</pre>
  </div>
  <div class="tab-pane" id="node18">
  <pre>
var id = '97167'
api.delete('/zones/pull.json' + id, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp18">
  <pre>
Console.Write("Zone id to delete: \n");
int id = Convert.ToInt32(Console.ReadLine());

api.Delete("/zones/pull.json/" + id);
</pre>
  </div>
  <div class="tab-pane" id="response18">
    <pre>
{
  "code":200
}</pre>
  </div>
</div>

## Enable Pull Zone

Enables a pull zone specified by the {zone_id} parameter

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/pull/{zone_id}/enable.json</span></div>
</div>


### Code Samples

<ul class="nav nav-tabs" id="myTab19">
  <li class="active"><a href="#ruby19" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python19" data-toggle='tab'>Python</a></li>
  <li><a href="#perl19" data-toggle='tab'>Perl</a></li>
  <li><a href="#php19" data-toggle='tab'>PHP</a></li>
  <li><a href="#node19" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp19" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response19" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby19">
    <pre>
id = '97167'
api.put('/zones/pull/'+id+'/enable.json')</pre>
  </div>
  <div class="tab-pane" id="python19">
    <pre>
id = '97167'
api.put('/zones/pull/'+id+'/enable.json')</pre>
  </div>
    <div class="tab-pane" id="perl19">
    <pre>
my $id = 134458;
$api->put("/zones/pull/" . $id . "/enable.json");</pre>
  </div>
  <div class="tab-pane" id="php19">
    <pre>
$id = '97167';
$api->put('/zones/pull/'.$id.'/enable.json');</pre>
  </div>
  <div class="tab-pane" id="node19">
  <pre>
var id = '97167'
api.put('/zones/pull/' + id + '/enable.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp19">
  <pre>
Console.Write("Zone id to enable: \n");
int id = Convert.ToInt32(Console.ReadLine());

api.Put("/zones/pull/" + id + "/enable.json");
</pre>
  </div>
  <div class="tab-pane" id="response19">
    <pre>
{
  "code":200
}
</pre>
  </div>
</div>

## Disable Pull Zone

Disables a pull zone specified by the {zone_id} parameter

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/pull/{zone_id}/disable.json</span></div>
</div>


### Code Samples

<ul class="nav nav-tabs" id="myTab20">
  <li class="active"><a href="#ruby20" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python20" data-toggle='tab'>Python</a></li>
  <li><a href="#perl20" data-toggle='tab'>Perl</a></li>
  <li><a href="#php20" data-toggle='tab'>PHP</a></li>
  <li><a href="#node20" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp20" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response20" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby20">
    <pre>
id = '97167'
api.put('/zones/pull/'+id+'/disable.json')</pre>
  </div>
  <div class="tab-pane" id="python20">
    <pre>
id = '97167'
api.put('/zones/pull/'+id+'/disable.json')</pre>
  </div>
    <div class="tab-pane" id="perl20">
    <pre>
my $id = 134458;
$api->put("/zones/pull/" . $id . "/disable.json");</pre>
  </div>
  <div class="tab-pane" id="php20">
    <pre>
$id = '97167';
$api->put('/zones/pull'.$id.'disable.json);</pre>
  </div>
  <div class="tab-pane" id="node20">
  <pre>
var id = '97167'
api.put('/zones/pull' + id + 'disable.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp20">
  <pre>
Console.Write("Zone id to disable: \n");
int id = Convert.ToInt32(Console.ReadLine());

api.Put("/zones/pull/" + id + "/disable.json");
</pre>
  </div>
  <div class="tab-pane" id="response20">
    <pre>
{
  "code":200
}</pre>
  </div>
</div>

## Purge Cache

Purges pull zone cache

<div class="heading">
<div class="url DELETE"><span class="http_method">DELETE</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/pull.json/{zone_id}/cache</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`files` | - | An array containing relative paths of the files to purge (i.e./favicon.ico) |

### Code Samples

<ul class="nav nav-tabs" id="myTab21">
  <li class="active"><a href="#ruby21" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python21" data-toggle='tab'>Python</a></li>
  <li><a href="#perl21" data-toggle='tab'>Perl</a></li>
  <li><a href="#php21" data-toggle='tab'>PHP</a></li>
  <li><a href="#node21" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp21" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response21" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby21">
  <pre>
#Purge Zone
id = '97167'
api.purge(id)

#Purge File
id = '97167'
api.purge(id,'/file1.txt')

#Purge Files
id = '97167'
api.purge(id, ['/file1.txt','/file2.txt'])</pre>
  </div>
  <div class="tab-pane" id="python21">
  <pre>
#Purge Zone
id = '97167'
api.purge(id)

#Purge File
id = '97167'
api.purge(id,'/file1.txt')

#Purge Files
id = '97167'
api.purge(id, ['/file1.txt','/file2.txt'])</pre>
  </div>
    <div class="tab-pane" id="perl21">
  <pre>
#Purge Zone
$api->delete("/zones/pull.json/165013/cache");

#Purge File
my @params = ("%2Frankings%2Fhotlist%2Fi%2F500w%2F2.jpg");
$api->delete("/zones/pull.json/165013/cache", @params);

#Purge Files
my @params = ("%2Frankings%2Fhotlist%2Fi%2F500w%2F2.jpg", "%2F_index%2Ff_mdcdb.html");
$api->delete("/zones/pull.json/165013/cache", @params);</pre>
  </div>
  <div class="tab-pane" id="php21">
    <pre>
//Purge Zone
$id = '97792';
$api->delete('/zones/pull.json/'.$id.'/cache');

//Purge File
$id = '97792';
$params = array('file'=>'/index.html');
$api->delete('/zones/pull.json/'.$id.'/cache',$params);

//Purge Files
$id = '97792';
$params = array(
    'files' => array(
        '/file1.txt',
        '/file2.txt'
    )
);
$api->delete('/zones/pull.json/'.$id.'/cache',$params);</pre>
  </div>
  <div class="tab-pane" id="node21">
  <pre>
// Purge Zone
var id = '96167'
api.delete('/zones/pull.json/' + id + '/cache', callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}

// Purge File
var id = '96167'
var file = '/file1.txt'
api.delete('/zones/pull.json/' + id + '/cache', file, callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}

// Purge File
var id = '96167'
var files = [ '/file1.txt', '/file2.txt' ]
api.delete('/zones/pull.json/' + id + '/cache', files, callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
  <div class="tab-pane" id="csharp21">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("What do you want to purge? (all/file)");
string ptype = Console.ReadLine();
switch (ptype){
	case "all":
	//Purge ALL
	api.Delete("/zones/pull.json/" + zoneID + "/cache");
	break;
	case "file":
	//Purge FILE
	Console.Write("Enter File Path to Purge (relative path): \n");
	string file = Console.ReadLine();
	file = "file=" + file;
	api.Purge("/zones/pull.json/" + zoneID + "/cache", file);
	break;
	case "fileS":
	//Purge FILES
	Console.Write("How Many? \n");
	int loop = Convert.ToInt32(Console.ReadLine());
	Console.Write("Enter File Paths to Purge (relative paths): \n");
	string files = "";
	for (int i = 0; i < loop; i++)
	{
		Console.Write(i + 1 + ": \n");
		string File = Console.ReadLine();
		files += "file[" + i + "]=" + File + "&";
	}
	api.Purge("/zones/pull.json/" + zoneID + "/cache", files);
	break;
}
</pre>
  </div>
  <div class="tab-pane" id="response21">
    <pre>
{
    "code": 200
}</pre>
  </div>
</div>

# Pull Zone Custom Domains API

## List Custom Domains

Returns a list of all custom domains on the zone specified by
{zone_id}

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/pull/{zone_id}/customdomains.json</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The id of the custom domain |
`bucket_id` | The id of the zone the custom domain belongs to |
`custom_domain` | A valid custom domain |

### Code Samples

<ul class="nav nav-tabs" id="myTab22">
  <li class="active"><a href="#ruby22" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python22" data-toggle='tab'>Python</a></li>
  <li><a href="#perl22" data-toggle='tab'>Perl</a></li>
  <li><a href="#php22" data-toggle='tab'>PHP</a></li>
  <li><a href="#node22" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp22" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response22" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby22">
    <pre>
id = '97167'
api.get('/zones/pull/'+id+'/customdomains.json')</pre>
  </div>
  <div class="tab-pane" id="python22">
    <pre>
id = '97167'
api.get('/zones/pull/'+id+'/customdomains.json')</pre>
  </div>
    <div class="tab-pane" id="perl22">
    <pre>
my $id = 134458;
$api->get("/zones/pull/" . $id . "/customdomains.json");
</pre>
  </div>
  <div class="tab-pane" id="php22">
    <pre>
$id = '96061';
$api->get('/zones/pull/'.$id.'/customdomains.json');</pre>
  </div>
  <div class="tab-pane" id="node22">
  <pre>
var id = '96061'
api.get('/zones/pull/' + id + '/customdomains.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp22">
  <pre>
Console.Write("Zone Id: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());

Console.Write(api.Get("/zones/pull/" + zoneID + "/customdomains.json"));
</pre>
  </div>
  <div class="tab-pane" id="response22">
    <pre>
{
    "code": 200,
    "data": {
        "customdomains": [
            {
                "bucket_id": "97167",
                "custom_domain": "cdn.somenewdomain.com",
                "id": "79182",
                "type": null
            }
        ],
        "total": 1
    }
}</pre>
  </div>
</div>

## Create Custom Domain

Adds a new custom domain to {zone_id}

<div class="heading">
<div class="url POST"><span class="http_method">POST</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/pull/{zone_id}/customdomains.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`custom_domain` | - | <span class="label important">required</span><br />length: 1-255 chars, valid::custom_domain, !valid::full_domain | A valid custom domain |
`type` | - | Applies only to VOD Zones and must be either 'vod-rtmp','vod-pseudo', 'vod-direct', or 'vod-ftp' | The type of custom domain being created |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The id of the custom domain |
`bucket_id` | The id of the zone the custom domain belongs to |
`custom_domain` | The valid custom domain |


### Code Samples

<ul class="nav nav-tabs" id="myTab23">
  <li class="active"><a href="#ruby23" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python23" data-toggle='tab'>Python</a></li>
  <li><a href="#perl23" data-toggle='tab'>Perl</a></li>
  <li><a href="#php23" data-toggle='tab'>PHP</a></li>
  <li><a href="#node23" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp23" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response23" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby23">
    <pre>
id = '97167'
params = {"custom_domain"=>"cdn.somedomain14.com"}
api.post('/zones/pull/'+id+'/customdomains.json', params)</pre>
  </div>
  <div class="tab-pane" id="python23">
    <pre>
id = '97167'
params = {"custom_domain":"cdn.somedomain13.com"}
api.post('/zones/pull/'+id+'/customdomains.json', params)</pre>
  </div>
    <div class="tab-pane" id="perl23">
    <pre>
my $id = 134458;
my @params = {custom_domain => 'idabic.dom.net'};
$api->post("/zones/pull/" . $id . "/customdomains.json", @params);</pre>
  </div>
  <div class="tab-pane" id="php23">
    <pre>
$id = '97167';
$params = array("custom_domain"=>"cdn.somedomain3.com");
$api->post('/zones/pull/'.$id.'/customdomains.json', $params);</pre>
  </div>
  <div class="tab-pane" id="node23">
  <pre>
var id = '96167'
api.post('/zones/pull/' + id + '/customdomains.json', { custom_domain: 'cdn.somedomain3.com' }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp23">
  <pre>
Console.Write("Zone Id: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Custom Domain: \n");
string dat = Console.ReadLine();

api.Post("/zones/pull/" + zoneID + "/customdomains.json", dat="custom_domain=" + dat);
</pre>
  </div>
  <div class="tab-pane" id="response23">
    <pre>
{
    "code": 201,
    "data": {
        "customdomain": {
            "bucket_id": "97167",
            "custom_domain": "cdn.somedomain3.com",
            "id": 79282,
            "type": null
        }
    }
}</pre>
  </div>
</div>

## Get Custom Domain

Gets a custom domain specified by the {zone_id} and
{customdomain_id} parameters

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/pull/{zone_id}/customdomains.json/{customdomain_id}</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The id of the custom domain |
`bucket_id` | The id of the zone the custom domain belongs to |
`custom_domain` | The valid custom domain |

### Code Samples

<ul class="nav nav-tabs" id="myTab24">
  <li class="active"><a href="#ruby24" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python24" data-toggle='tab'>Python</a></li>
  <li><a href="#perl24" data-toggle='tab'>Perl</a></li>
  <li><a href="#php24" data-toggle='tab'>PHP</a></li>
  <li><a href="#node24" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp24" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response24" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby24">
    <pre>
zoneId = '97167'
domainId = '79182'
api.get('/zones/pull/'+zoneId+'/customdomains.json/'+domainId)</pre>
  </div>
  <div class="tab-pane" id="python24">
    <pre>
zoneId = '97167'
domainId = '79182'
api.get('/zones/pull/'+zoneId+'/customdomains.json/'+domainId)</pre>
  </div>
    <div class="tab-pane" id="perl24">
    <pre>
my $zid = 134458;
my $cid = 113070;
my $data = $api->get("/zones/pull/" . $zid . "/customdomains.json/" . $cid);
print $data->{'customdomain'}{'custom_domain'};</pre>
  </div>
  <div class="tab-pane" id="php24">
    <pre>
$zoneId = '97167';
$domainId = '79182';
$api->get('/zones/pull/'.$zoneId.'/customdomains.json/'.$domainId);</pre>
  </div>
  <div class="tab-pane" id="node24">
  <pre>
var id = '97167'
var domainId = '79182'
api.get('/zones/pull/' + id + '/customdomains.json/' + domainId, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp24">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Custom Domain Id: \n");
int domainId = Convert.ToInt32(Console.ReadLine());

api.Get("/zones/pull/" + zoneID + "/customdomains.json/" + domainId);
</pre>
  </div>
  <div class="tab-pane" id="response24">
    <pre>
{
    "code": 200,
    "data": {
        "customdomain": {
            "bucket_id": "97167",
            "custom_domain": "cdn.somenewdomain.com",
            "id": "79182",
            "type": null
        }
    }
}
</pre>
  </div>
</div>

## Update Custom Domain

Updates a custom domain specified by the id parameter

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/pull/{zone_id}/customdomains.json/{customdomain_id}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`custom_domain` | - | <span class="label important">required</span><br />length: 1-255 chars, valid::custom_domain, !valid::full_domain | A new valid custom domain |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The id of the custom domain |
`bucket_id` | The id of the zone the custom domain belongs to |
`custom_domain` | The new valid custom domain |


### Code Samples

<ul class="nav nav-tabs" id="myTab25">
  <li class="active"><a href="#ruby25" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python25" data-toggle='tab'>Python</a></li>
  <li><a href="#perl25" data-toggle='tab'>Perl</a></li>
  <li><a href="#php25" data-toggle='tab'>PHP</a></li>
  <li><a href="#node25" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp25" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response25" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby25">
    <pre>
zoneId = '97167'
domainId = '79182'
params = {"custom_domain"=>"cdn.somenewdomain41.com"}
api.put('/zones/pull/'+zoneId+'/customdomains.json/'+domainId,params)</pre>
  </div>
  <div class="tab-pane" id="python25">
    <pre>
zoneId = '97167'
domainId = '79182'
params = {"custom_domain":"cdn.somenewdomain41.com"}
api.put('/zones/pull/'+zoneId+'/customdomains.json/'+domainId,params=params)</pre>
  </div>
    <div class="tab-pane" id="perl25">
    <pre>
my $zid = 134458;
my $cid = 173075;
my @params = ('custom_domain=idabic.domain.net');
$api->put("/zones/pull/" . $zid . "/customdomains.json/" . $cid, @params);</pre>
  </div>
  <div class="tab-pane" id="php25">
    <pre>
$zoneId = '97167';
$domainId = '79182';
$params = array("custom_domain"=>"cdn.somenewdomain.com");
$api->put('/zones/pull/'.$zoneId.'/customdomains.json/'.$domainId, $params);</pre>
  </div>
  <div class="tab-pane" id="node25">
  <pre>
var zoneId = '97167'
var domainId = '79182'
api.put('/zones/pull/' + zoneId + '/customdomains.json/' + domainId, { custom_domain: 'cdn.somenewdomain.com' }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp25">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Custom Doamin Id to Edit: \n");
int domainId = Convert.ToInt32(Console.ReadLine());
Console.Write("New Value for this custom domain: \n");
string cdname = Console.ReadLine();

api.Put("/zones/pull/" + zoneID + "/customdomains.json/" + domainId, "custom_domain=" + cdname);
</pre>
  </div>
  <div class="tab-pane" id="response25">
    <pre>
{
    "code": 200,
    "data": {
        "customdomain": {
            "bucket_id": "97167",
            "custom_domain": "cdn.somenewdomain4.com",
            "id": "79182",
            "type": null
        }
    }
}</pre>
  </div>
</div>

## Delete Custom Domain

Deletes a custom domain specified by the {zone_id} and
{customdomain_id} parameters

<div class="heading">
<div class="url DELETE"><span class="http_method">DELETE</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/pull/{zone_id}/customdomains.json/{customdomain_id}</span></div>
</div>


### Code Samples

<ul class="nav nav-tabs" id="myTab26">
  <li class="active"><a href="#ruby26" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python26" data-toggle='tab'>Python</a></li>
  <li><a href="#perl26" data-toggle='tab'>Perl</a></li>
  <li><a href="#php26" data-toggle='tab'>PHP</a></li>
  <li><a href="#node26" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp26" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response26" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby26">
    <pre>
zoneId = '97167'
domainId = '79182'
api.delete('/zones/pull/'+zoneId+'/customdomains.json/'+domainId)</pre>
  </div>
  <div class="tab-pane" id="python26">
    <pre>
zoneId = '97167'
domainId = '79182'
api.delete('/zones/pull/'+zoneId+'/customdomains.json/'+domainId)</pre>
  </div>
    <div class="tab-pane" id="perl26">
    <pre>
my $zid = 134458;
my $cid = 173075;
$api->delete("/zones/pull/" . $zid . "/customdomains.json/" . $cid);</pre>
  </div>
  <div class="tab-pane" id="php26">
    <pre>
$zoneId = '97167';
$domainId = '79182';
$api->delete('/zones/pull/'.$zoneId.'/customdomains.json/'.$domainId);</pre>
  </div>
  <div class="tab-pane" id="node26">
  <pre>
var zoneId = '97167'
var domainId = '79182'
api.delete('/zones/pull/' + zoneId + '/customdomains.json/' + domainId, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp26">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Custom Doamin Id to Edit: \n");
int domainId = Convert.ToInt32(Console.ReadLine());

api.Delete("/zones/pull/" + zoneID + "/customdomains.json/" + domainId);
</pre>
  </div>
  <div class="tab-pane" id="response26">
    <pre>
{
  "code":200
}</pre>
  </div>
</div>

# Push Zone API

## List Push Zones

Returns a list of all push zones on the specified account

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/push.json</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | Push Zone ID |
`name` | Push Zone name |
`label` | Something that describes your zone |
`valid_referers` | List of domains for http referrer protection (separated by space), only the domains in the list will be treated as valid referrers |
`content_disposition` | Force files to download |
`sslshared` | Enable Shared SSL for your zone, so you can use HTTPS, using our SSL certificate for netdna-ssl.com |
`suspend` | Flag denoting if the zone has been suspended |
`locked` | Flag denoting if the zone has been locked |
`inactive` | Flag denoting if the zone has been deleted |
`creation_date` | Date Created |
`spdy` | Flag denoting if the zone has the SPDY protocol enabled |

### Code Samples

<ul class="nav nav-tabs" id="myTab27">
  <li class="active"><a href="#ruby27" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python27" data-toggle='tab'>Python</a></li>
  <li><a href="#perl27" data-toggle='tab'>Perl</a></li>
  <li><a href="#php27" data-toggle='tab'>PHP</a></li>
  <li><a href="#node27" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp27" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response27" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby27">
    <pre>
api.get('/zones/push.json')</pre>
  </div>
  <div class="tab-pane" id="python27">
    <pre>
api.get('/zones/push.json')</pre>
  </div>
    <div class="tab-pane" id="perl27">
    <pre>
$api->get("/zones/push.json")</pre>
  </div>
  <div class="tab-pane" id="php27">
    <pre>
$api->get('/zones/push.json');</pre>
  </div>
  <div class="tab-pane" id="node27">
  <pre>
api.get('/zones/push.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp27">
  <pre>
api.Get("/zones/push.json");
</pre>
  </div>
  <div class="tab-pane" id="response27">
    <pre>
{
    "code": 200,
    "data": {
        "current_page_size": 2,
        "page": 1,
        "page_size": "50",
        "pages": 1,
        "pushzones": [
            {
                "cdn_url": "cdn.somedomain.net",
                "compress": "0",
                "content_disposition": "0",
                "creation_date": "2013-05-16 15:25:19",
                "expires": null,
                "ftp_url": "ftp.newpushzone2.alias.netdna-cdn.com",
                "id": "96182",
                "inactive": "0",
                "label": null,
                "locked": "0",
                "name": "newpushzone2",
                "server_id": "11",
                "sslshared": "0",
                "storage_updated": "2013-05-24 06:31:52",
                "storage_used": "20480",
                "suspend": "0",
                "tmp_url": "newpushzone2.alias.netdna-cdn.com",
                "type": "3",
                "valid_referers": null,
                "spdy": 1
            },
            {
                "cdn_url": "cdn.somenewdomain2.com",
                "compress": "0",
                "content_disposition": "0",
                "creation_date": "2013-05-23 21:01:39",
                "expires": null,
                "ftp_url": "ftp.newpushzone3.alias.netdna-cdn.com",
                "id": "97181",
                "inactive": "0",
                "label": "Some other description",
                "locked": "0",
                "name": "newpushzone3",
                "server_id": "11",
                "sslshared": "0",
                "storage_updated": "2013-05-24 06:31:52",
                "storage_used": "20480",
                "suspend": "0",
                "tmp_url": "newpushzone3.alias.netdna-cdn.com",
                "type": "3",
                "valid_referers": null,
                "spdy": 0
            }
        ],
        "total": 2
    }
}</pre>
  </div>
</div>


## Create Push Zone

Creates a new push zone

<div class="heading">
<div class="url POST"><span class="http_method">POST</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/push.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`name` | - | <span class="label important">required</span><br />length: 3-30 chars; only letters, digits, and dash (-)accepted | Push Zone name |
`password` | - | <span class="label important">required</span><br />length: 5-30 chars; | Push Zone FTP password |
`label` | - | length: 1-255 chars | Something that describes your zone |
`valid_referers` | - | length: 1-200 chars | List of domains for http referrer protection (separated by space), only the domains in the list will be treated as valid referrers |
`content_disposition` | 0 | only 0 or 1 accepted | Force files to download |
`sslshared` | 0 | only 0 or 1 accepted | Enable Shared SSL for your zone, so you can use HTTPS, using our SSL certificate for netdna-ssl.com |
`spdy` | 0 | only 0 or 1 accepted | Enable SPDY protocol on the zone (requires SSL) |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | Push Zone ID |
`name` | Push Zone name |
`label` | Something that describes your zone |
`valid_referers` | List of domains for http referrer protection (separated by space), only the domains in the list will be treated as valid referrers |
`content_disposition` | Force files to download |
`sslshared` | Enable Shared SSL for your zone, so you can use HTTPS, using our SSL certificate for netdna-ssl.com |
`suspend` | Flag denoting if the zone has been suspended |
`locked` | Flag denoting if the zone has been locked |
`inactive` | Flag denoting if the zone has been deleted |
`creation_date` | Date Created |
`spdy` | Flag denoting if the zone has the SPDY protocol enabled |

### Code Samples

<ul class="nav nav-tabs" id="myTab28">
  <li class="active"><a href="#ruby28" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python28" data-toggle='tab'>Python</a></li>
  <li><a href="#perl28" data-toggle='tab'>Perl</a></li>
  <li><a href="#php28" data-toggle='tab'>PHP</a></li>
  <li><a href="#node28" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp28" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response28" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby28">
    <pre>
params = {"name"=>"newPushZone99","password"=>"password"}
api.post('/zones/push.json',params)</pre>
  </div>
  <div class="tab-pane" id="python28">
    <pre>
params = {"name":"newPushZone6","password":"password"}
api.post('/zones/push.json',data=params)</pre>
  </div>
    <div class="tab-pane" id="perl28">
    <pre>
my @params = {name => 'perltestpush', password => 'password'};
$api->post("/zones/push.json", @params);</pre>
  </div>
  <div class="tab-pane" id="php28">
    <pre>
$params = array("name"=>"newPushZone","password"=>"password");
$api->post('/zones/push.json', $params);</pre>
  </div>
  <div class="tab-pane" id="node28">
  <pre>
api.post('/zones/push.json', { name: 'newPushZone', password: 'password' }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp28">
  <pre>
Console.Write("Zone Name: \n");
string ZoneName = Console.ReadLine();
Console.Write("Password: \n");
string password = Console.ReadLine();

api.Post("/zones/push.json", "name=" + ZoneName + "&password=" + password);
</pre>
  </div>
  <div class="tab-pane" id="response28">
    <pre>
{
    "code": 201,
    "data": {
        "pushzone": {
            "cdn_url": "newpushzone4.alias.netdna-cdn.com",
            "compress": 0,
            "content_disposition": 0,
            "creation_date": "2013-05-24 16:41:53",
            "expires": null,
            "ftp_url": "ftp.newpushzone4.alias.netdna-cdn.com",
            "id": 97317,
            "inactive": 0,
            "label": null,
            "locked": 0,
            "name": "newpushzone4",
            "server_id": "11",
            "sslshared": null,
            "storage_updated": null,
            "storage_used": null,
            "suspend": 0,
            "tmp_url": "newpushzone4.alias.netdna-cdn.com",
            "type": 3,
            "valid_referers": null,
            "spdy": 1
        }
    }
}</pre>
  </div>
</div>


## Get Push Zones Count

Counts all push zones on the specified account

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/push.json/count</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`count` | The number of push zones on the specified account |

### Code Samples

<ul class="nav nav-tabs" id="myTab29">
  <li class="active"><a href="#ruby29" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python29" data-toggle='tab'>Python</a></li>
  <li><a href="#perl29" data-toggle='tab'>Perl</a></li>
  <li><a href="#php29" data-toggle='tab'>PHP</a></li>
  <li><a href="#node29" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp29" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response29" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby29">
    <pre>
api.get('/zones/push.json/count')</pre>
  </div>
  <div class="tab-pane" id="python29">
    <pre>
api.get('/zones/push.json/count')</pre>
  </div>
    <div class="tab-pane" id="perl29">
    <pre>
$api->get("/zones/push.json/count");</pre>
  </div>
  <div class="tab-pane" id="php29">
    <pre>
$api->get('/zones/push.json/count');</pre>
  </div>
  <div class="tab-pane" id="node29">
  <pre>
api.get('/zones/push.json/count', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp29">
  <pre>
Console.Write("Zone id: \n");
int id = Convert.ToInt32(Console.ReadLine());

api.Get("/zones/push.json/" + id);
</pre>
  </div>
  <div class="tab-pane" id="response29">
    <pre>
{
    "code": 200,
    "data": {
        "count": "3"
    }
}
</pre>
  </div>
</div>


## Get Push Zone

Gets a push zone specified by the {zone_id} parameter

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/push.json/{zone_id}</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | Push Zone ID |
`name` | Push Zone name |
`label` | Something that describes your zone |
`valid_referers` | List of domains for http referrer protection (separated by space), only the domains in the list will be treated as valid referrers |
`content_disposition` | Force files to download |
`sslshared` | Enable Shared SSL for your zone, so you can use HTTPS, using our SSL certificate for netdna-ssl.com |
`suspend` | Flag denoting if the zone has been suspended |
`locked` | Flag denoting if the zone has been locked |
`inactive` | Flag denoting if the zone has been deleted |
`creation_date` | Date Created |
`spdy` | Flag denoting if the zone has the SPDY protocol enabled |

### Code Samples

<ul class="nav nav-tabs" id="myTab30">
  <li class="active"><a href="#ruby30" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python30" data-toggle='tab'>Python</a></li>
  <li><a href="#perl30" data-toggle='tab'>Perl</a></li>
  <li><a href="#php30" data-toggle='tab'>PHP</a></li>
  <li><a href="#node30" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp30" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response30" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby30">
    <pre>
id = '97793'
api.get('/zones/push.json/'+id)</pre>
  </div>
  <div class="tab-pane" id="python30">
    <pre>
id = '96182'
api.get('/zones/push.json/'+id)</pre>
  </div>
    <div class="tab-pane" id="perl30">
    <pre>
my $id = 55659;
$api->get("/zones/push.json/" . $id);</pre>
  </div>
  <div class="tab-pane" id="php30">
    <pre>
$id = '97181';
$api->get('/zones/push.json/'.$id);</pre>
  </div>
  <div class="tab-pane" id="node30">
  <pre>
var id = '97182'
api.get('/zones/push.json/' + id, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp30">
  <pre>Console.Write("Zone id: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
api.Get("/zones/push.json/" + zoneID);
</pre>
  </div>
  <div class="tab-pane" id="response30">
    <pre>
{
    "code": 200,
    "data": {
        "pushzone": {
            "cdn_url": "cdn.somenewdomain2.com",
            "compress": "0",
            "content_disposition": "0",
            "creation_date": "2013-05-23 21:01:39",
            "expires": null,
            "ftp_url": "ftp.newpushzone3.alias.netdna-cdn.com",
            "id": "97181",
            "inactive": "0",
            "label": "Some other description",
            "locked": "0",
            "name": "newpushzone3",
            "server_id": "11",
            "sslshared": "0",
            "storage_updated": "2013-05-24 06:31:52",
            "storage_used": "20480",
            "suspend": "0",
            "tmp_url": "newpushzone3.alias.netdna-cdn.com",
            "type": "3",
            "valid_referers": null,
            "spdy": 1
        }
    }
}</pre>
  </div>
</div>


## Update Push Zone

Updates a push zone specified by the {zone_id} parameter

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/push.json/{zone_id}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`label` | - | length: 1-255 chars | Something that describes your zone |
`valid_referers` | - | length: 1-100 chars | List of domains for http referrer protection (separated by space), only the domains in the list will be treated as valid referrers |
`content_disposition` | 0 | only 0 or 1 accepted | Force files to download |
`sslshared` | 0 | only 0 or 1 accepted | Enable Shared SSL for your zone, so you can use HTTPS, using our SSL certificate for netdna-ssl.com |
`spdy` | 0 | only 0 or 1 accepted | Enable SPDY protocol on the zone (requires SSL) |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | Push Zone ID |
`name` | Push Zone name |
`label` | Something that describes your zone |
`valid_referers` | List of domains for http referrer protection (separated by space), only the domains in the list will be treated as valid referrers |
`content_disposition` | Force files to download |
`sslshared` | Enable Shared SSL for your zone, so you can use HTTPS, using our SSL certificate for netdna-ssl.com |
`suspend` | Flag denoting if the zone has been suspended |
`locked` | Flag denoting if the zone has been locked |
`inactive` | Flag denoting if the zone has been deleted |
`creation_date` | Date Created |
`spdy` | Flag denoting if the zone has the SPDY protocol enabled |

### Code Samples

<ul class="nav nav-tabs" id="myTab31">
  <li class="active"><a href="#ruby31" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python31" data-toggle='tab'>Python</a></li>
  <li><a href="#perl31" data-toggle='tab'>Perl</a></li>
  <li><a href="#php31" data-toggle='tab'>PHP</a></li>
  <li><a href="#node31" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp31" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response31" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby31">
    <pre>
id = '97793'
params = {"label"=>"Some other description"}
api.put('/zones/push.json/'+id,params)</pre>
  </div>
  <div class="tab-pane" id="python31">
    <pre>
id = '96182'
params = {"label":"Some other description"}
api.put('/zones/push.json/'+id,params=params)</pre>
  </div>
    <div class="tab-pane" id="perl31">
    <pre>
my $id = 55659;
my @params = ('compress=0');
$api->put("/zones/push.json/" . $id, @params);</pre>
  </div>
  <div class="tab-pane" id="php31">
    <pre>
$id = '97181';
$params = array("label"=>"Some other description");
$api->put('/zones/push.json/'.$id, $params);</pre>
  </div>
  <div class="tab-pane" id="node31">
  <pre>
var id = '97182'
api.put('/zones/push.json/' + id, { label: 'Some other description' }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp31">
  <pre>
Console.Write("Zone id to edit: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Property to edit/change (label/compression...): \n");
string prop = Console.ReadLine();
Console.Write("New value: \n");
string val = Console.ReadLine();

api.Put("/zones/push.json/" + zoneID, prop + "=" + val);
</pre>
  </div>
  <div class="tab-pane" id="response31">
    <pre>
{
    "code": 200,
    "data": {
        "pushzone": {
            "cdn_url": "cdn.somenewdomain2.com",
            "compress": "0",
            "content_disposition": "0",
            "creation_date": "2013-05-23 21:01:39",
            "expires": null,
            "ftp_url": "ftp.newpushzone3.alias.netdna-cdn.com",
            "id": "97181",
            "inactive": "0",
            "label": "Some other description",
            "locked": "0",
            "name": "newpushzone3",
            "server_id": "11",
            "sslshared": "0",
            "storage_updated": "2013-05-24 06:31:52",
            "storage_used": "20480",
            "suspend": "0",
            "tmp_url": "newpushzone3.alias.netdna-cdn.com",
            "type": "3",
            "valid_referers": null,
            "spdy": 1
        }
    }
}</pre>
  </div>
</div>


## Delete Push Zone

Deletes a push zone specified by the {zone_id} parameter

<div class="heading">
<div class="url DELETE"><span class="http_method">DELETE</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/push.json/{zone_id}</span></div>
</div>

### Code Samples

<ul class="nav nav-tabs" id="myTab32">
  <li class="active"><a href="#ruby32" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python32" data-toggle='tab'>Python</a></li>
  <li><a href="#perl32" data-toggle='tab'>Perl</a></li>
  <li><a href="#php32" data-toggle='tab'>PHP</a></li>
  <li><a href="#node32" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp32" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response32" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby32">
    <pre>
id = '97793'
api.delete('/zones/push.json/'+id)</pre>
  </div>
  <div class="tab-pane" id="python32">
    <pre>
id = '96182'
api.delete('/zones/push.json/'+id)</pre>
  </div>
    <div class="tab-pane" id="perl32">
    <pre>
my $id = 55659;
$api->delete("/zones/push.json/" . $id);</pre>
  </div>
  <div class="tab-pane" id="php32">
    <pre>
$id = '97181';
$api->delete('/zones/push.json/'.$id);</pre>
  </div>
  <div class="tab-pane" id="node32">
  <pre>
var id = '97181'
api.delete('/zones/push.json/' + id, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp32">
  <pre>
Console.Write("Zone id to delete: \n");
int id = Convert.ToInt32(Console.ReadLine());

api.Delete("/zones/push.json/" + id);
</pre>
  </div>
  <div class="tab-pane" id="response32">
    <pre>
{
  "code":200
}</pre>
  </div>
</div>


## Enable Push Zone

Enables a push zone specified by the {zone_id} parameter

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/push/{zone_id}/enable.json</span></div>
</div>

### Code Samples

<ul class="nav nav-tabs" id="myTab33">
  <li class="active"><a href="#ruby33" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python33" data-toggle='tab'>Python</a></li>
  <li><a href="#perl33" data-toggle='tab'>Perl</a></li>
  <li><a href="#php33" data-toggle='tab'>PHP</a></li>
  <li><a href="#node33" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp33" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response33" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby33">
    <pre>
id = '97793'
api.put('/zones/push/'+id+'/enable.json')</pre>
  </div>
  <div class="tab-pane" id="python33">
    <pre>
id = '96182'
api.put('/zones/push/'+id+'/enable.json')</pre>
  </div>
    <div class="tab-pane" id="perl33">
    <pre>
my $id = 55659;
$api->put("/zones/push/" . $id . "/enable.json");</pre>
  </div>
  <div class="tab-pane" id="php33">
    <pre>
$id = '97181';
$api->put('/zones/push/'.$id.'/enable.json');</pre>
  </div>
  <div class="tab-pane" id="node33">
  <pre>
var id = '97181'
api.put('/zones/push/' + id + '/enable.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp33">
  <pre>
Console.Write("Zone id to enable: \n");
int id = Convert.ToInt32(Console.ReadLine());

api.Put("/zones/push/" + id + "/enable.json");
</pre>
  </div>
  <div class="tab-pane" id="response33">
    <pre>
{
  "code":200
}</pre>
  </div>
</div>


## Disable Push Zone

Disables a push zone specified by the {zone_id} parameter

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/push/{zone_id}/disable.json</span></div>
</div>


### Code Samples

<ul class="nav nav-tabs" id="myTab34">
  <li class="active"><a href="#ruby34" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python34" data-toggle='tab'>Python</a></li>
  <li><a href="#perl34" data-toggle='tab'>Perl</a></li>
  <li><a href="#php34" data-toggle='tab'>PHP</a></li>
  <li><a href="#node34" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp34" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response34" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby34">
    <pre>
id = '97793'
api.put('/zones/push/'+id+'/disable.json')</pre>
  </div>
  <div class="tab-pane" id="python34">
    <pre>
id = '96182'
api.put('/zones/push/'+id+'/disable.json')</pre>
  </div>
    <div class="tab-pane" id="perl34">
    <pre>
my $id = 55659;
$api->put("/zones/push/" . $id . "/disable.json");</pre>
  </div>
  <div class="tab-pane" id="php34">
    <pre>
$id = '97181';
$api->put('/zones/push/'.$id.'/disable.json');</pre>
  </div>
  <div class="tab-pane" id="node34">
  <pre>
var id = '97181'
api.put('/zones/push/' + id + '/disable.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp34">
  <pre>
Console.Write("Zone id to disable: \n");
int id = Convert.ToInt32(Console.ReadLine());

api.Put("/zones/push/" + id + "/disable.json");
</pre>
  </div>
  <div class="tab-pane" id="response34">
    <pre>
{
  "code":200
}</pre>
  </div>
</div>


# Push Zone Custom Domains API

## List Custom Domains

Returns a list of all custom domains on the zone specified by
{zone_id}

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/push/{zone_id}/customdomains.json</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The id of the custom domain |
`bucket_id` | The id of the zone the custom domain belongs to |
`custom_domain` | A valid custom domain |

### Code Samples

<ul class="nav nav-tabs" id="myTab35">
  <li class="active"><a href="#ruby35" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python35" data-toggle='tab'>Python</a></li>
  <li><a href="#perl35" data-toggle='tab'>Perl</a></li>
  <li><a href="#php35" data-toggle='tab'>PHP</a></li>
  <li><a href="#node35" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp35" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response35" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby35">
    <pre>
id = '97793'
api.get('/zones/push/'+id+'/customdomains.json')</pre>
  </div>
  <div class="tab-pane" id="python35">
    <pre>
id = '96182'
api.get('/zones/push/'+id+'/customdomains.json')</pre>
  </div>
    <div class="tab-pane" id="perl35">
    <pre>
my $id = 134458;
$api->get("/zones/push/" . $id . "/customdomains.json");</pre>
  </div>
  <div class="tab-pane" id="php35">
    <pre>
$id = '96061';
$api->get('/zones/push/'.$id.'/customdomains.json');</pre>
  </div>
  <div class="tab-pane" id="node35">
  <pre>
var id = '96061'
api.get('/zones/push/' + id + '/customdomains.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp35">
  <pre>
Console.Write("Zone Id: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());

Console.Write(api.Get("/zones/push/" + zoneID + "/customdomains.json"));
</pre>
  </div>
  <div class="tab-pane" id="response35">
    <pre>
{
    "code": 200,
    "data": {
        "customdomains": [
            {
                "bucket_id": "96061",
                "custom_domain": "cdn.somedomain.com",
                "id": "78330",
                "type": null
            }
        ],
        "total": 1
    }
}</pre>
  </div>
</div>


## Create Custom Domain

Adds a new custom domain to {zone_id}

<div class="heading">
<div class="url POST"><span class="http_method">POST</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/push/{zone_id}/customdomains.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`custom_domain` | - | <span class="label important">required</span><br />length: 1-255 chars, valid::custom_domain, !valid::full_domain | A valid custom domain |
`type` | - | Applies only to VOD Zones and must be either 'vod-rtmp','vod-pseudo', 'vod-direct', or 'vod-ftp' | The type of custom domain being created |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The id of the custom domain |
`bucket_id` | The id of the zone the custom domain belongs to |
`custom_domain` | The valid custom domain |

### Code Samples

<ul class="nav nav-tabs" id="myTab36">
  <li class="active"><a href="#ruby36" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python36" data-toggle='tab'>Python</a></li>
  <li><a href="#perl36" data-toggle='tab'>Perl</a></li>
  <li><a href="#php36" data-toggle='tab'>PHP</a></li>
  <li><a href="#node36" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp36" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response36" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby36">
    <pre>
id = '97793'
params = {"custom_domain"=>"cdn.somedomain19.com"}
api.post('/zones/push/'+id+'/customdomains.json', params)</pre>
  </div>
  <div class="tab-pane" id="python36">
    <pre>
id = '96182'
params = {"custom_domain":"cdn.somedomain15.com"}
api.post('/zones/push/'+id+'/customdomains.json', params)</pre>
  </div>
    <div class="tab-pane" id="perl36">
    <pre>
my $id = 55659;
my @params = {custom_domain => 'idabic2.dom.net'};
$api->post("/zones/push/" . $id . "/customdomains.json", @params);</pre>
  </div>
  <div class="tab-pane" id="php36">
    <pre>
$id = '97181';
$params = array("custom_domain"=>"cdn.somedomain2.net");
$api->post('/zones/push/'.$id.'/customdomains.json', $params);</pre>
  </div>
  <div class="tab-pane" id="node36">
  <pre>
var id = '97181'
api.post('/zones/push/' + id + '/customdomains.json', { custom_domain: 'cdn.somedomain2.net' }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp36">
  <pre>
Console.Write("Zone Id: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Custom Domain: \n");
string dat = Console.ReadLine();

api.Post("/zones/push/" + zoneID + "/customdomains.json", dat="custom_domain=" + dat);
</pre>
  </div>
  <div class="tab-pane" id="response36">
    <pre>
{
    "code": 201,
    "data": {
        "customdomain": {
            "bucket_id": "97181",
            "custom_domain": "cdn.somedomain4.net",
            "id": 79283,
            "type": null
        }
    }
}
</pre>
  </div>
</div>


## Get Custom Domain

Gets a custom domain specified by the {zone_id} and
{customdomain_id} parameters

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/push/{zone_id}/customdomains.json/{customdomain_id}</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The id of the custom domain |
`bucket_id` | The id of the zone the custom domain belongs to |
`custom_domain` | The valid custom domain |

### Code Samples

<ul class="nav nav-tabs" id="myTab37">
  <li class="active"><a href="#ruby37" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python37" data-toggle='tab'>Python</a></li>
  <li><a href="#perl37" data-toggle='tab'>Perl</a></li>
  <li><a href="#php37" data-toggle='tab'>PHP</a></li>
  <li><a href="#node37" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp37" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response37" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby37">
    <pre>
zoneId = '97793'
domainId = '79747'
api.get('/zones/push/'+zoneId+'/customdomains.json/'+domainId)</pre>
  </div>
  <div class="tab-pane" id="python37">
    <pre>
zoneId = '96182'
domainId = '79320'
api.get('/zones/push/'+zoneId+'/customdomains.json/'+domainId)</pre>
  </div>
    <div class="tab-pane" id="perl37">
    <pre>
my $zid = 55659;
my $cid = 122211;
$api->get("/zones/push/" . $zid . "/customdomains.json/" . $cid);</pre>
  </div>
  <div class="tab-pane" id="php37">
    <pre>
$zoneId = '97181';
$domainId = '79188';
$api->get('/zones/push/'.$zoneId.'/customdomains.json/'.$domainId);</pre>
  </div>
  <div class="tab-pane" id="node37">
  <pre>
var zoneId = '97181'
var domainId = '79188'
api.get('/zones/push/' + zoneId + '/customdomains.json/' + domainId, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp37">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Custom Domain Id: \n");
int domainId = Convert.ToInt32(Console.ReadLine());

api.Get("/zones/push/" + zoneID + "/customdomains.json/" + domainId);
</pre>
  </div>
  <div class="tab-pane" id="response37">
    <pre>
{
    "code": 200,
    "data": {
        "customdomain": {
            "bucket_id": "97181",
            "custom_domain": "cdn.somenewdomain2.com",
            "id": "79188",
            "type": null
        }
    }
}</pre>
  </div>
</div>


## Update Custom Domain

Updates a custom domain specified by the id parameter

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/push/{zone_id}/customdomains.json/{customdomain_id}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`custom_domain` | - | <span class="label important">required</span><br />length: 1-255 chars, valid::custom_domain, !valid::full_domain | A new valid custom domain |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The id of the custom domain |
`bucket_id` | The id of the zone the custom domain belongs to |
`custom_domain` | The new valid custom domain |

### Code Samples

<ul class="nav nav-tabs" id="myTab38">
  <li class="active"><a href="#ruby38" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python38" data-toggle='tab'>Python</a></li>
  <li><a href="#perl38" data-toggle='tab'>Perl</a></li>
  <li><a href="#php38" data-toggle='tab'>PHP</a></li>
  <li><a href="#node38" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp38" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response38" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby38">
    <pre>
zoneId = '97793'
domainId = '79747'
params = {"custom_domain"=>"cdn.somenewdomain41.com"}
api.put('/zones/push/'+zoneId+'/customdomains.json/'+domainId,params)</pre>
  </div>
  <div class="tab-pane" id="python38">
    <pre>
zoneId = '96182'
domainId = '79320'
params = {"custom_domain":"cdn.somenewdomain40.com"}
api.put('/zones/push/'+zoneId+'/customdomains.json/'+domainId,params=params)</pre>
  </div>
    <div class="tab-pane" id="perl38">
    <pre>
my $zid = 55659;
my $cid = 122211;
my @params = ('custom_domain=idabic.domain.net');
$api->put("/zones/push/" . $zid . "/customdomains.json/" . $cid, @params);</pre>
  </div>
  <div class="tab-pane" id="php38">
    <pre>
$zoneId = '97181';
$domainId = '79188';
$params = array("custom_domain"=>"cdn.somenewdomain2.com");
$api->put('/zones/push/'.$zoneId.'/customdomains.json/'.$domainId, $params);
</pre>
  </div>
  <div class="tab-pane" id="node38">
  <pre>
var zoneId = '97181'
var domainId = '79188'
api.put('/zones/push/' + zoneId + '/customdomains.json/' + domainId, { custom_domain: 'cdn.somenewdomain2.com' }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp38">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Custom Doamin Id to Edit: \n");
int domainId = Convert.ToInt32(Console.ReadLine());
Console.Write("New Value for this custom domain: \n");
string cdname = Console.ReadLine();

api.Put("/zones/push/" + zoneID + "/customdomains.json/" + domainId, "custom_domain=" + cdname);
</pre>
  </div>
  <div class="tab-pane" id="response38">
    <pre>
{
    "code": 200,
    "data": {
        "customdomain": {
            "bucket_id": "97181",
            "custom_domain": "cdn.somenewdomain12.com",
            "id": "79188",
            "type": null
        }
    }
}</pre>
  </div>
</div>


## Delete Custom Domain

Deletes a custom domain specified by the {zone_id} and
{customdomain_id} parameters

<div class="heading">
<div class="url DELETE"><span class="http_method">DELETE</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/push/{zone_id}/customdomains.json/{customdomain_id}</span></div>
</div>


### Code Samples

<ul class="nav nav-tabs" id="myTab39">
  <li class="active"><a href="#ruby39" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python39" data-toggle='tab'>Python</a></li>
  <li><a href="#perl39" data-toggle='tab'>Perl</a></li>
  <li><a href="#php39" data-toggle='tab'>PHP</a></li>
  <li><a href="#node39" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp39" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response39" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby39">
    <pre>
zoneId = '97793'
domainId = '79747'
api.delete('/zones/push/'+zoneId+'/customdomains.json/'+domainId)</pre>
  </div>
  <div class="tab-pane" id="python39">
    <pre>
zoneId = '96182'
domainId = '79320'
api.delete('/zones/push/'+zoneId+'/customdomains.json/'+domainId)</pre>
  </div>
    <div class="tab-pane" id="perl39">
    <pre>
my $zid = 55659;
my $cid = 122211;
$api->delete("/zones/push/" . $zid . "/customdomains.json/" . $cid);</pre>
  </div>
  <div class="tab-pane" id="php39">
    <pre>
$zoneId = '97181';
$domainId = '79188';
$api->delete('/zones/push/'.$zoneId.'/customdomains.json/'.$domainId);</pre>
  </div>
  <div class="tab-pane" id="node39">
  <pre>
var zoneId = '97181'
var domainId = '79188'
api.delete('/zones/push/' + zoneId + '/customdomains.json/' + domainId, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp39">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Custom Doamin Id to Edit: \n");
int domainId = Convert.ToInt32(Console.ReadLine());

api.Delete("/zones/push/" + zoneID + "/customdomains.json/" + domainId);
</pre>
  </div>
  <div class="tab-pane" id="response39">
    <pre>
{
  "code":200
}</pre>
  </div>
</div>


# VOD Zone API

## List VOD Zones

Returns a list of all VOD zones on the specified account

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/vod.json</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | VOD Zone ID |
`name` | VOD Zone name |
`label` | The zone's description |
`suspend` | Flag denoting if the zone has been suspended |
`locked` | Flag denoting if the zone has been locked |
`inactive` | Flag denoting if the zone has been deleted |
`creation_date` | Date Created |

### Code Samples

<ul class="nav nav-tabs" id="myTab40">
  <li class="active"><a href="#ruby40" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python40" data-toggle='tab'>Python</a></li>
  <li><a href="#perl40" data-toggle='tab'>Perl</a></li>
  <li><a href="#php40" data-toggle='tab'>PHP</a></li>
  <li><a href="#node40" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp40" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response40" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby40">
    <pre>
api.get('/zones/vod.json')</pre>
  </div>
  <div class="tab-pane" id="python40">
    <pre>
api.get('/zones/vod.json')</pre>
  </div>
    <div class="tab-pane" id="perl40">
    <pre>
$api->get("/zones/vod.json")</pre>
  </div>
  <div class="tab-pane" id="php40">
    <pre>
$api->get('/zones/vod.json');</pre>
  </div>
  <div class="tab-pane" id="node40">
  <pre>
api.get('/zones/vod.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp40">
  <pre>
api.Get("/zones/vod.json");
</pre>
  </div>
  <div class="tab-pane" id="response40">
    <pre>
{
    "code": 200,
    "data": {
        "current_page_size": 2,
        "page": 1,
        "page_size": "50",
        "pages": 1,
        "total": 2,
        "vodzones": [
            {
                "cdn_url": "cdn.somedomain.com",
                "creation_date": "2013-05-16 16:02:35",
                "direct_url": "d.newvodzone.alias.netdna-cdn.com",
                "ftp_url": "ftp.newvodzone.alias.netdna-cdn.com",
                "id": "96187",
                "inactive": "0",
                "label": null,
                "locked": "0",
                "name": "newvodzone",
                "pseudo_url": "p.newvodzone.alias.netdna-cdn.com",
                "rtmp_url": "r.newvodzone.alias.netdna-cdn.com",
                "server_id": "30",
                "storage_updated": "2013-05-24 06:35:35",
                "storage_used": "4096",
                "suspend": "0",
                "tmp_url": "newvodzone.alias.netdna-cdn.com",
                "token": null,
                "type": "4"
            },
            {
                "cdn_url": "cdn.somenewdomain3.com",
                "creation_date": "2013-05-23 21:25:44",
                "direct_url": "d.newvodzone3.alias.netdna-cdn.com",
                "ftp_url": "ftp.newvodzone3.alias.netdna-cdn.com",
                "id": "97183",
                "inactive": "0",
                "label": "Some other description",
                "locked": "0",
                "name": "newvodzone3",
                "pseudo_url": "p.newvodzone3.alias.netdna-cdn.com",
                "rtmp_url": "r.newvodzone3.alias.netdna-cdn.com",
                "server_id": "30",
                "storage_updated": "2013-05-24 06:35:35",
                "storage_used": "4096",
                "suspend": "0",
                "tmp_url": "newvodzone3.alias.netdna-cdn.com",
                "token": null,
                "type": "4"
            }
        ]
    }
}</pre>
  </div>
</div>


## Create VOD Zone

Creates a new VOD zone

<div class="heading">
<div class="url POST"><span class="http_method">POST</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/vod.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`name` | - | <span class="label important">required</span><br />length: 3-30 chars; only letters, digits, and dash (-)accepted | VOD Zone user name |
`password` | - | <span class="label important">required</span><br />length: 5-30 chars | Your desired password |
`token` | - | length: 1-64 chars | The token value (shared secret) for secure streaming |
`label` | - | length: 1-255 chars | Something that describes your zone |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | VOD Zone ID |
`name` | VOD Zone name |
`label` | The zone's description |
`suspend` | Flag denoting if the zone has been suspended |
`locked` | Flag denoting if the zone has been locked |
`inactive` | Flag denoting if the zone has been deleted |
`creation_date` | Date Created |

### Code Samples

<ul class="nav nav-tabs" id="myTab41">
  <li class="active"><a href="#ruby41" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python41" data-toggle='tab'>Python</a></li>
  <li><a href="#perl41" data-toggle='tab'>Perl</a></li>
  <li><a href="#php41" data-toggle='tab'>PHP</a></li>
  <li><a href="#node41" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp41" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response41" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby41">
    <pre>
params = {"name"=>"newVodZone99","password"=>"password"}
api.post('/zones/vod.json',params)</pre>
  </div>
  <div class="tab-pane" id="python41">
    <pre>
params = {"name":"newvodZone7","password":"password"}
api.post('/zones/vod.json',data=params)</pre>
  </div>
    <div class="tab-pane" id="perl41">
    <pre>
my @params = {name => 'perltest5', password => 'password'};
$api->post("/zones/vod.json", @params);</pre>
  </div>
  <div class="tab-pane" id="php41">
    <pre>
$params = array("name"=>"newVODZone3","password"=>"password");
$api->post('/zones/vod.json',$params);</pre>
  </div>
  <div class="tab-pane" id="node41">
  <pre>
api.post('/zones/vod.json', { name: 'newVODZone3', password: 'password' }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp41">
  <pre>
Console.Write("Zone Name: \n");
string ZoneName = Console.ReadLine();
Console.Write("Password: \n");
string password = Console.ReadLine();

api.Post("/zones/vod.json", "name=" + ZoneName + "&password=" + password);
</pre>
  </div>
  <div class="tab-pane" id="response41">
    <pre>
{
    "code": 201,
    "data": {
        "vodzone": {
            "cdn_url": "newvodzone4.alias.netdna-cdn.com",
            "creation_date": "2013-05-24 16:50:18",
            "direct_url": "d.newvodzone4.alias.netdna-cdn.com",
            "ftp_url": "ftp.newvodzone4.alias.netdna-cdn.com",
            "id": 97319,
            "inactive": 0,
            "label": null,
            "locked": 0,
            "name": "newvodzone4",
            "pseudo_url": "p.newvodzone4.alias.netdna-cdn.com",
            "rtmp_url": "r.newvodzone4.alias.netdna-cdn.com",
            "server_id": "30",
            "storage_updated": null,
            "storage_used": null,
            "suspend": 0,
            "tmp_url": "newvodzone4.alias.netdna-cdn.com",
            "token": null,
            "type": 4
        }
    }
}</pre>
  </div>
</div>


## Get VOD Zones Count

Counts all VOD zones on the specified account

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/vod.json/count</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`count` | The number of VOD zones on the specified account |

### Code Samples

<ul class="nav nav-tabs" id="myTab42">
  <li class="active"><a href="#ruby42" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python42" data-toggle='tab'>Python</a></li>
  <li><a href="#perl42" data-toggle='tab'>Perl</a></li>
  <li><a href="#php42" data-toggle='tab'>PHP</a></li>
  <li><a href="#node42" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp42" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response42" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby42">
    <pre>
api.get('/zones/vod.json/count')</pre>
  </div>
  <div class="tab-pane" id="python42">
    <pre>
api.get('/zones/vod.json/count')</pre>
  </div>
    <div class="tab-pane" id="perl42">
    <pre>
$api->get("/zones/vod.json/count")</pre>
  </div>
  <div class="tab-pane" id="php42">
    <pre>
$api->get('/zones/vod.json/count');</pre>
  </div>
  <div class="tab-pane" id="node42">
  <pre>
api.get('/zones/vod.json/count', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp42">
  <pre>
api.Get("/zones/vod.json/count");
</pre>
  </div>
  <div class="tab-pane" id="response42">
    <pre>
{
    "code": 200,
    "data": {
        "count": "4"
    }
}</pre>
  </div>
</div>


## Get VOD Zone

Gets a VOD zone specified by the {zone_id} parameter

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/vod.json/{zone_id}</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | VOD Zone ID |
`name` | VOD Zone name |
`label` | The zone's description |
`suspend` | Flag denoting if the zone has been suspended |
`locked` | Flag denoting if the zone has been locked |
`inactive` | Flag denoting if the zone has been deleted |
`creation_date` | Date Created |

### Code Samples

<ul class="nav nav-tabs" id="myTab43">
  <li class="active"><a href="#ruby43" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python43" data-toggle='tab'>Python</a></li>
  <li><a href="#perl43" data-toggle='tab'>Perl</a></li>
  <li><a href="#php43" data-toggle='tab'>PHP</a></li>
  <li><a href="#node43" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp43" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response43" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby43">
    <pre>
id = '97794'
api.get('/zones/vod.json/'+id)</pre>
  </div>
  <div class="tab-pane" id="python43">
    <pre>
id = '96187'
api.get('/zones/vod.json/'+id)</pre>
  </div>
    <div class="tab-pane" id="perl43">
    <pre>
my $id = 75477;
$api->get("/zones/vod.json/" . $id);</pre>
  </div>
  <div class="tab-pane" id="php43">
    <pre>
$id = '97183';
$api->get('/zones/vod.json/'.$id);</pre>
  </div>
  <div class="tab-pane" id="node43">
  <pre>
var id = '97183'
api.get('/zones/vod.json/' + id, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp43">
  <pre>
Console.Write("Zone id: \n");
int id = Convert.ToInt32(Console.ReadLine());

api.Get("/zones/vod.json/" + id);
</pre>
  </div>
  <div class="tab-pane" id="response43">
    <pre>
{
    "code": 200,
    "data": {
        "vodzone": {
            "cdn_url": "cdn.somenewdomain3.com",
            "creation_date": "2013-05-23 21:25:44",
            "direct_url": "d.newvodzone3.alias.netdna-cdn.com",
            "ftp_url": "ftp.newvodzone3.alias.netdna-cdn.com",
            "id": "97183",
            "inactive": "0",
            "label": "Some other description",
            "locked": "0",
            "name": "newvodzone3",
            "pseudo_url": "p.newvodzone3.alias.netdna-cdn.com",
            "rtmp_url": "r.newvodzone3.alias.netdna-cdn.com",
            "server_id": "30",
            "storage_updated": "2013-05-24 06:35:35",
            "storage_used": "4096",
            "suspend": "0",
            "tmp_url": "newvodzone3.alias.netdna-cdn.com",
            "token": null,
            "type": "4"
        }
    }
}</pre>
  </div>
</div>


## Update VOD Zone

Updates a VOD zone specified by the {zone_id} parameter

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/vod.json/{zone_id}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`password` | - | length: 5-30 chars | Your desired password |
`token` | - | length: 1-64 chars | The token value (shared secret) for secure streaming |
`label` | - | length: 1-255 chars | Something that describes your zone |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | VOD Zone ID |
`name` | VOD Zone name |
`label` | The zone's description |
`suspend` | Flag denoting if the zone has been suspended |
`locked` | Flag denoting if the zone has been locked |
`inactive` | Flag denoting if the zone has been deleted |
`creation_date` | Date Created |

### Code Samples

<ul class="nav nav-tabs" id="myTab44">
  <li class="active"><a href="#ruby44" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python44" data-toggle='tab'>Python</a></li>
  <li><a href="#perl44" data-toggle='tab'>Perl</a></li>
  <li><a href="#php44" data-toggle='tab'>PHP</a></li>
  <li><a href="#node44" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp44" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response44" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby44">
    <pre>
id = '97794'
params = {"label"=>"Some other description"}
api.put('/zones/vod.json/'+id,params)</pre>
  </div>
  <div class="tab-pane" id="python44">
    <pre>
id = '96187'
params = {"label":"Some other description"}
api.put('/zones/vod.json/'+id,params=params)</pre>
  </div>
    <div class="tab-pane" id="perl44">
    <pre>
my $id = 75477;
my @params = ('compress=0');
$api->put("/zones/vod.json/" . $id, @params);</pre>
  </div>
  <div class="tab-pane" id="php44">
    <pre>
$id = '97183';
$params =  array("label"=>"Some other description");
$api->put('/zones/vod.json/'.$id,$params);</pre>
  </div>
  <div class="tab-pane" id="node44">
  <pre>
var id = '97183'
api.put('/zones/vod.json/' + id, { label: 'Some other description' }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp44">
  <pre>
Console.Write("Zone id to edit: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Property to edit/change (label...): \n");
string prop = Console.ReadLine();
Console.Write("New value: \n");
string val = Console.ReadLine();

api.Put("/zones/vod.json/" + zoneID, prop + "=" + val);
</pre>
  </div>
  <div class="tab-pane" id="response44">
    <pre>
{
    "code": 200,
    "data": {
        "vodzone": {
            "cdn_url": "cdn.somenewdomain3.com",
            "creation_date": "2013-05-23 21:25:44",
            "direct_url": "d.newvodzone3.alias.netdna-cdn.com",
            "ftp_url": "ftp.newvodzone3.alias.netdna-cdn.com",
            "id": "97183",
            "inactive": "0",
            "label": "Some other description",
            "locked": "0",
            "name": "newvodzone3",
            "pseudo_url": "p.newvodzone3.alias.netdna-cdn.com",
            "rtmp_url": "r.newvodzone3.alias.netdna-cdn.com",
            "server_id": "30",
            "storage_updated": "2013-05-24 06:35:35",
            "storage_used": "4096",
            "suspend": "0",
            "tmp_url": "newvodzone3.alias.netdna-cdn.com",
            "token": null,
            "type": "4"
        }
    }
}</pre>
  </div>
</div>


## Delete VOD Zone

Deletes a VOD zone specified by the {zone_id} parameter

<div class="heading">
<div class="url DELETE"><span class="http_method">DELETE</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/vod.json/{zone_id}</span></div>
</div>

### Code Samples

<ul class="nav nav-tabs" id="myTab45">
  <li class="active"><a href="#ruby45" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python45" data-toggle='tab'>Python</a></li>
  <li><a href="#perl45" data-toggle='tab'>Perl</a></li>
  <li><a href="#php45" data-toggle='tab'>PHP</a></li>
  <li><a href="#node45" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp45" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response45" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby45">
    <pre>
id = '97794'
api.delete('/zones/vod.json/'+id)</pre>
  </div>
  <div class="tab-pane" id="python45">
    <pre>
id = '96187'
api.delete('/zones/vod.json/'+id)</pre>
  </div>
    <div class="tab-pane" id="perl45">
    <pre>
my $id = 75477;
$api->delete("/zones/vod.json/" . $id);</pre>
  </div>
  <div class="tab-pane" id="php45">
    <pre>
$id = '97183';
$api->delete('/zones/vod.json/'.$id);</pre>
  </div>
  <div class="tab-pane" id="node45">
  <pre>
var id = '97183'
api.delete('/zones/vod.json/' + id, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp45">
  <pre>
Console.Write("Zone id to delete: \n");
int id = Convert.ToInt32(Console.ReadLine());

api.Delete("/zones/vod.json/" + id);
</pre>
  </div>
  <div class="tab-pane" id="response45">
    <pre>
{
  "code":200
}</pre>
  </div>
</div>


## Enable VOD Zone

Enables a VOD zone specified by the {zone_id} parameter

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/vod/{zone_id}/enable.json</span></div>
</div>

### Code Samples

<ul class="nav nav-tabs" id="myTab46">
  <li class="active"><a href="#ruby46" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python46" data-toggle='tab'>Python</a></li>
  <li><a href="#perl46" data-toggle='tab'>Perl</a></li>
  <li><a href="#php46" data-toggle='tab'>PHP</a></li>
  <li><a href="#node46" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp46" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response46" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby46">
    <pre>
id = '97794'
api.put('/zones/vod/'+id+'/enable.json')</pre>
  </div>
  <div class="tab-pane" id="python46">
    <pre>
id = '96187'
api.put('/zones/vod/'+id+'/enable.json')</pre>
  </div>
    <div class="tab-pane" id="perl46">
    <pre>
my $id = 75477;
$api->put("/zones/vod/" . $id . "/enable.json");</pre>
  </div>
  <div class="tab-pane" id="php46">
    <pre>
$id = '96187';
$api->put('/zones/vod/'.$id.'/enable.json');</pre>
  </div>
  <div class="tab-pane" id="node46">
  <pre>
var id = '96187'
api.put('/zones/vod/' + id + '/enable.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp46">
  <pre>
Console.Write("Zone id to enable: \n");
int id = Convert.ToInt32(Console.ReadLine());

api.Put("/zones/vod/" + id + "/enable.json");
</pre>
  </div>
  <div class="tab-pane" id="response46">
    <pre>
{
  "code":200
}</pre>
  </div>
</div>


## Disable VOD Zone

Disables a VOD zone specified by the {zone_id} parameter

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/vod/{zone_id}/disable.json</span></div>
</div>

### Code Samples

<ul class="nav nav-tabs" id="myTab47">
  <li class="active"><a href="#ruby47" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python47" data-toggle='tab'>Python</a></li>
  <li><a href="#perl47" data-toggle='tab'>Perl</a></li>
  <li><a href="#php47" data-toggle='tab'>PHP</a></li>
  <li><a href="#node47" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp47" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response47" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby47">
    <pre>
id = '97794'
api.put('/zones/vod/'+id+'/disable.json')</pre>
  </div>
  <div class="tab-pane" id="python47">
    <pre>
id = '96187'
api.put('/zones/vod/'+id+'/disable.json')</pre>
  </div>
    <div class="tab-pane" id="perl47">
    <pre>
my $id = 75477;
$api->put("/zones/vod/" . $id . "/disable.json");</pre>
  </div>
  <div class="tab-pane" id="php47">
    <pre>
$id = '96187';
$api->put('/zones/vod/'.$id.'/disable.json');</pre>
  </div>
  <div class="tab-pane" id="node47">
  <pre>
var id = '96187'
api.put('/zones/vod/' + id + '/disable.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp47">
  <pre>
Console.Write("Zone id to disable: \n");
int id = Convert.ToInt32(Console.ReadLine());

api.Put("/zones/vod/" + id + "/disable.json");
</pre>
  </div>
  <div class="tab-pane" id="response47">
    <pre>
{
  "code":200
}</pre>
  </div>
</div>


# VOD Zone Custom Domains API

## List Custom Domains

Returns a list of all custom domains on the zone specified by
{zone_id}

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/vod/{zone_id}/customdomains.json</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The id of the custom domain |
`bucket_id` | The id of the zone the custom domain belongs to |
`custom_domain` | A valid custom domain |

### Code Samples

<ul class="nav nav-tabs" id="myTab48">
  <li class="active"><a href="#ruby48" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python48" data-toggle='tab'>Python</a></li>
  <li><a href="#perl48" data-toggle='tab'>Perl</a></li>
  <li><a href="#php48" data-toggle='tab'>PHP</a></li>
  <li><a href="#node48" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp48" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response48" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby48">
    <pre>
id = '97794'
api.get('/zones/vod/'+id+'/customdomains.json')</pre>
  </div>
  <div class="tab-pane" id="python48">
    <pre>
id = '96187'
api.get('/zones/vod/'+id+'/customdomains.json')</pre>
  </div>
    <div class="tab-pane" id="perl48">
    <pre>
my $id = 75477;
$api->get("/zones/vod/" . $id . "/customdomains.json");</pre>
  </div>
  <div class="tab-pane" id="php48">
    <pre>
$id = '97183';
$api->get('/zones/vod/'.$id.'/customdomains.json');</pre>
  </div>
  <div class="tab-pane" id="node48">
  <pre>
var id = '97183'
api.get('/zones/vod.json/' + id + '/customdomains.json, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp48">
  <pre>
Console.Write("Zone Id: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());

Console.Write(api.Get("/zones/vod/" + zoneID + "/customdomains.json"));
</pre>
  </div>
  <div class="tab-pane" id="response48">
    <pre>
{
    "code": 200,
    "data": {
        "customdomains": [
            {
                "bucket_id": "97183",
                "custom_domain": "cdn.somenewdomain3.com",
                "id": "79191",
                "type": "vod-rtmp"
            }
        ],
        "total": 1
    }
}</pre>
  </div>
</div>


## Create Custom Domain

Adds a new custom domain to {zone_id}

<div class="heading">
<div class="url POST"><span class="http_method">POST</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/vod/{zone_id}/customdomains.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`custom_domain` | - | <span class="label important">required</span><br />length: 1-255 chars, valid::custom_domain, !valid::full_domain | A valid custom domain |
`type` | - | Applies only to VOD Zones and must be either 'vod-rtmp','vod-pseudo', 'vod-direct', or 'vod-ftp' | The type of custom domain being created |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The id of the custom domain |
`bucket_id` | The id of the zone the custom domain belongs to |
`custom_domain` | The valid custom domain |

### Code Samples

<ul class="nav nav-tabs" id="myTab49">
  <li class="active"><a href="#ruby49" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python49" data-toggle='tab'>Python</a></li>
  <li><a href="#perl49" data-toggle='tab'>Perl</a></li>
  <li><a href="#php49" data-toggle='tab'>PHP</a></li>
  <li><a href="#node49" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp49" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response49" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby49">
    <pre>
id = '97794'
params = {"custom_domain"=>"cdn.somedomain39.com","type"=>"vod-rtmp"}
api.post('/zones/vod/'+id+'/customdomains.json', params)</pre>
  </div>
  <div class="tab-pane" id="python49">
    <pre>
id = '96187'
params = {"custom_domain":"cdn.somedomain16.com","type":"vod-rtmp"}
api.post('/zones/vod/'+id+'/customdomains.json', params)</pre>
  </div>
    <div class="tab-pane" id="perl49">
    <pre>
my $id = 75477;
my @params = {custom_domain => 'idabic3.dom.net', type => 'vod-rtmp'};
$api->post("/zones/vod/" . $id . "/customdomains.json", @params);</pre>
  </div>
  <div class="tab-pane" id="php49">
    <pre>
$id = '97183';
$params = array("custom_domain"=>"cdn.somedomain2.com","type"=>"vod-rtmp");
$api->post('/zones/vod/'.$id.'/customdomains.json', $params);</pre>
  </div>
  <div class="tab-pane" id="node49">
  <pre>
var id = '97183'
api.post('/zones/vod/' + id + '/customdomains.json', { custom_domain: 'cdn.somedomain2.com', type: 'vod-rtmp' }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp49">
  <pre>
Console.Write("Zone Id: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Custom Domain: \n");
string dat = Console.ReadLine();
Console.Write("Type: (vod-rtmp, vod-pseudo, vod-direct, or vod-ftp)\n");
string cdtype = Console.ReadLine();

api.Post("/zones/vod/" + zoneID + "/customdomains.json", dat="custom_domain=" + dat + "&type=" + cdtype);
</pre>
  </div>
  <div class="tab-pane" id="response49">
    <pre>
{
    "code": 201,
    "data": {
        "customdomain": {
            "bucket_id": "97183",
            "custom_domain": "cdn.somedomain2.com",
            "id": 79284,
            "type": "vod-rtmp"
        }
    }
}</pre>
  </div>
</div>


## Get Custom Domain

Gets a custom domain specified by the {zone_id} and
{customdomain_id} parameters

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/vod/{zone_id}/customdomains.json/{customdomain_id}</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The id of the custom domain |
`bucket_id` | The id of the zone the custom domain belongs to |
`custom_domain` | The valid custom domain |

### Code Samples

<ul class="nav nav-tabs" id="myTab50">
  <li class="active"><a href="#ruby50" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python50" data-toggle='tab'>Python</a></li>
  <li><a href="#perl50" data-toggle='tab'>Perl</a></li>
  <li><a href="#php50" data-toggle='tab'>PHP</a></li>
  <li><a href="#node50" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp50" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response50" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby50">
    <pre>
zoneId = '97794'
domainId = '79748'
api.get('/zones/vod/'+zoneId+'/customdomains.json/'+domainId)</pre>
  </div>
  <div class="tab-pane" id="python50">
    <pre>
zoneId = '96187'
domainId = '79321'
api.get('/zones/vod/'+zoneId+'/customdomains.json/'+domainId)</pre>
  </div>
    <div class="tab-pane" id="perl50">
    <pre>
my $zid = 75477;
my $cid = 173088;
my $data = $api->get("/zones/vod/" . $zid . "/customdomains.json/" . $cid);</pre>
  </div>
  <div class="tab-pane" id="php50">
    <pre>
$zoneId = '97183';
$domainId = '79191';
$api->get('/zones/vod/'.$zoneId.'/customdomains.json/'.$domainId);</pre>
  </div>
  <div class="tab-pane" id="node50">
  <pre>
var zoneId = '97183'
var domainId = '79191'
api.get('/zones/vod/' + zoneId + '/customdomains.json/' + domainId, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp50">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Custom Domain Id: \n");
int domainId = Convert.ToInt32(Console.ReadLine());

api.Get"/zones/vod/" + zoneID + "/customdomains.json/" + domainId);
</pre>
  </div>
  <div class="tab-pane" id="response50">
    <pre>
{
    "code": 200,
    "data": {
        "customdomain": {
            "bucket_id": "97183",
            "custom_domain": "cdn.somenewdomain3.com",
            "id": "79191",
            "type": "vod-rtmp"
        }
    }
}</pre>
  </div>
</div>


## Update Custom Domain

Updates a custom domain specified by the id parameter

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/vod/{zone_id}/customdomains.json/{customdomain_id}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`custom_domain` | - | <span class="label important">required</span><br />length: 1-255 chars, valid::custom_domain, !valid::full_domain | A new valid custom domain |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The id of the custom domain |
`bucket_id` | The id of the zone the custom domain belongs to |
`custom_domain` | The new valid custom domain |

### Code Samples

<ul class="nav nav-tabs" id="myTab51">
  <li class="active"><a href="#ruby51" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python51" data-toggle='tab'>Python</a></li>
  <li><a href="#perl51" data-toggle='tab'>Perl</a></li>
  <li><a href="#php51" data-toggle='tab'>PHP</a></li>
  <li><a href="#node51" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp51" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response51" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby51">
    <pre>
zoneId = '97794'
domainId = '79748'
params = {"custom_domain"=>"cdn.somenewdomain49.com"}
api.put('/zones/vod/'+zoneId+'/customdomains.json/'+domainId,params)</pre>
  </div>
  <div class="tab-pane" id="python51">
    <pre>
zoneId = '96187'
domainId = '79321'
params = {"custom_domain":"cdn.somenewdomain401.com"}
api.put('/zones/vod/'+zoneId+'/customdomains.json/'+domainId,params=params)</pre>
  </div>
    <div class="tab-pane" id="perl51">
    <pre>
my $zid = 75477;
my $cid = 173088;
my @params = ('custom_domain=idabic.domain.net');
$api->put("/zones/vod/" . $zid . "/customdomains.json/" . $cid, @params);</pre>
  </div>
  <div class="tab-pane" id="php51">
    <pre>
$zoneId = '97183';
$domainId = '79191';
$params = array("custom_domain"=>"cdn.somenewdomain3.com");
$api->put('/zones/vod/'.$zoneId.'/customdomains.json/'.$domainId, $params);</pre>
  </div>
  <div class="tab-pane" id="node51">
  <pre>
var zoneId = '97183'
var domainId = '79191'
api.put('/zones/vod/' + zoneId + '/customdomains.json/' + domainId, { custom_domain: 'cdn.somenewdomain3.com' }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp51">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Custom Doamin Id to Edit: \n");
int domainId = Convert.ToInt32(Console.ReadLine());
Console.Write("New Value for this custom domain: \n");
string cdname = Console.ReadLine();

api.Put("/zones/vod/" + zoneID + "/customdomains.json/" + domainId, "custom_domain=" + cdname);
</pre>
  </div>
  <div class="tab-pane" id="response51">
    <pre>
{
    "code": 200,
    "data": {
        "customdomain": {
            "bucket_id": "97183",
            "custom_domain": "cdn.somenewdomain42.com",
            "id": "79284",
            "type": "vod-rtmp"
        }
    }
}</pre>
  </div>
</div>


## Delete Custom Domain

Deletes a custom domain specified by the {zone_id} and
{customdomain_id} parameters

<div class="heading">
<div class="url DELETE"><span class="http_method">DELETE</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/vod/{zone_id}/customdomains.json/{customdomain_id}</span></div>
</div>


### Code Samples

<ul class="nav nav-tabs" id="myTab52">
  <li class="active"><a href="#ruby52" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python52" data-toggle='tab'>Python</a></li>
  <li><a href="#perl52" data-toggle='tab'>Perl</a></li>
  <li><a href="#php52" data-toggle='tab'>PHP</a></li>
  <li><a href="#node52" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp52" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response52" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby52">
    <pre>
zoneId = '97794'
domainId = '79748'
api.delete('/zones/vod/'+zoneId+'/customdomains.json/'+domainId)</pre>
  </div>
  <div class="tab-pane" id="python52">
    <pre>
zoneId = '96187'
domainId = '79321'
api.delete('/zones/vod/'+zoneId+'/customdomains.json/'+domainId)</pre>
  </div>
    <div class="tab-pane" id="perl52">
    <pre>
my $zid = 75477;
my $cid = 173088;
$api->delete("/zones/vod/" . $zid . "/customdomains.json/" . $cid);</pre>
  </div>
  <div class="tab-pane" id="php52">
    <pre>
$zoneId = '97183';
$domainId = '79191';
$api->delete('/zones/vod/'.$zoneId.'/customdomains.json/'.$domainId);</pre>
  </div>
  <div class="tab-pane" id="node52">
  <pre>
var zoneId = '97183'
var domainId = '79191'
api.delete('/zones/vod/' + zoneId + '/customdomains.json/' + domainId, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp52">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Custom Domain Id to Edit: \n");
int domainId = Convert.ToInt32(Console.ReadLine());

api.Delete("/zones/vod/" + zoneID + "/customdomains.json/" + domainId);
</pre>
  </div>
  <div class="tab-pane" id="response52">
    <pre>
{
  "code":200
}</pre>
  </div>
</div>


# Zones SSL API

## Get Zone's SSL Information

Get the SSL certificate for the specified {zone_type} and
{zone_id}.

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/{zone_type}/{zone_id}/ssl.json</span></div>
</div>

### Code Samples

<ul class="nav nav-tabs" id="myTab61">
  <li class="active"><a href="#ruby61" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python61" data-toggle='tab'>Python</a></li>
  <li><a href="#perl61" data-toggle='tab'>Perl</a></li>
  <li><a href="#php61" data-toggle='tab'>PHP</a></li>
  <li><a href="#node61" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp61" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response61" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby61">
    <pre>
id = '96061'
type = 'pull'
api.get('/zones/'+type+'/'+id+'/ssl.json')</pre>
  </div>
  <div class="tab-pane" id="python61">
    <pre>
id = '96061'
type = 'pull'
api.get('/zones/'+type+'/'+id+'/ssl.json')</pre>
  </div>
    <div class="tab-pane" id="perl61">
    <pre>
my $id = 236828;
my $type = "pull";
$api->get("/zones/" . $type . "/" . $id . "/ssl.json");</pre>
  </div>
  <div class="tab-pane" id="php61">
    <pre>
$id = '96061';
$type = 'pull';
$api->get('/zones/'.$type.'/'.$id.'/ssl.json');</pre>
  </div>
  <div class="tab-pane" id="node61">
  <pre>
var id = '96061'
var type = 'pull'
api.get('/zones/' + type + '/' + id + '/ssl.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp61">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Zone type: \n");
string type = Console.ReadLine();

api.Get("/zones/" + type + "/" + zoneID + "/ssl.json");
</pre>
  </div>
  <div class="tab-pane" id="response61">
    <pre>
{
  "code":201,
  "data":{
    "ssl":{
      "id":1459,
      "ssl_id":1234
      "ssl_crt":"-----BEGIN CERTIFICATE-----\n{ ... your certificate ... }\n-----END CERTIFICATE-----\n",
      "ssl_cabundle":null,
      "date_expiration":"2014-01-24",
      "anycast_ip_id":null,
      "wildcard":1,
      "domain":"*.idcreator.com"
    }
  }
}
</pre>
  </div>
</div>


## Install SSL on Zone

Upload an SSL certificate for the specified {zone_type} and
{zone_id}.

<div class="heading">
<div class="url POST"><span class="http_method">POST</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/{zone_type}/{zone_id}/ssl.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`ssl_id`  | - | digit | id of previously created certificate (NOTE: This will become required in future revisions)
`ssl_crt` | - | - | The SSL certificate you are installing. (NOTE: Not required if ssl_id specified) |
`ssl_key` | - | - | The key for the SSL certificate you are installing. |
`ssl_cabundle` | - | - | The CA Bundle for the SSL Certificate you are installing. |
`ssl_sni` | 0 | only 0 or 1 accepted | If this flag is set to 1 your zone will use SNI to identify your certificate, rather than requiring a dedicated IP. |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The SSL Certificate ID. |
`ssl_crt` | The SSL certificate. |
`ssl_cabundle` | The CA Bundle for the certificate. |
`domain` | The domain applicable to this certificate. |
`date_expiration` | The date of expiration for the certificate. |
`wildcard` | Flag to signify whether this is a wildcard certificate. |

### Code Samples

<ul class="nav nav-tabs" id="myTab62">
  <li class="active"><a href="#ruby62" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python62" data-toggle='tab'>Python</a></li>
  <li><a href="#perl62" data-toggle='tab'>Perl</a></li>
  <li><a href="#php62" data-toggle='tab'>PHP</a></li>
  <li><a href="#node62" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp62" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response62" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby62">
    <pre>
id = '96061'
type = 'pull'
ssl_crt = "-----BEGIN CERTIFICATE-----\n{ ... your certificate ... }\n-----END CERTIFICATE-----\n"
ssl_key = "-----BEGIN RSA PRIVATE KEY-----\n{ ... your key ... }\n-----END RSA PRIVATE KEY-----"
params = {"ssl_crt"=> ssl_crt,"ssl_key"=> ssl_key}
api.post('/zones/'+type+'/'+id+'/ssl.json',params)</pre>
  </div>
  <div class="tab-pane" id="python62">
    <pre>
id = '96061'
type = 'pull'
ssl_crt = "-----BEGIN CERTIFICATE-----\n{ ... your certificate ... }\n-----END CERTIFICATE-----\n"
ssl_key = "-----BEGIN RSA PRIVATE KEY-----\n{ ... your key ... }\n-----END RSA PRIVATE KEY-----"
params = {"ssl_crt": ssl_crt,"ssl_key": ssl_key}
api.post('/zones/'+type+'/'+id+'/ssl.json',params)</pre>
  </div>
    <div class="tab-pane" id="perl62">
    <pre>
my $id = 236828;
my $type = 'pull';
my $ssl_crt = "-----BEGIN CERTIFICATE-----\n{ ... your certificate ... }\n-----END CERTIFICATE-----\n";
my $ssl_key = "-----BEGIN RSA PRIVATE KEY-----\n{ ... your key ... }\n-----END RSA PRIVATE KEY-----";
my @params = {ssl_crt => $ssl_crt, ssl_key => $ssl_key};
$api->post("/zones/" . $type . "/" . $id . "/ssl.json", @params);</pre>
  </div>
  <div class="tab-pane" id="php62">
    <pre>
$id = '96061';
$type = 'pull';
$ssl_crt = "-----BEGIN CERTIFICATE-----\n{ ... your certificate ... }\n-----END CERTIFICATE-----\n";
$ssl_key = "-----BEGIN RSA PRIVATE KEY-----\n{ ... your key ... }\n-----END RSA PRIVATE KEY-----";
$params = array("ssl_crt"=>$ssl_crt,"ssl_key"=>$ssl_key);
$api->post('/zones/'.$type.'/'.$id.'/ssl.json',$params);</pre>
  </div>
  <div class="tab-pane" id="node62">
  <pre>
var id = '96061'
var type = 'pull'
var ssl_crt = "-----BEGIN CERTIFICATE-----\n{ ... your certificate ... }\n-----END CERTIFICATE-----\n"
var ssl_key = "-----BEGIN RSA PRIVATE KEY-----\n{ ... your key ... }\n-----END RSA PRIVATE KEY-----"
api.post('/zones/' + type + '/' + id + '/ssl.json', { ssl_crt: ssl_crt, ssl_key: ssl_key }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
    <div class="tab-pane" id="csharp62">
  <pre>
var cert = "";
var key = "";
Console.Write("Zone id: \n");
int zoneId = Convert.ToInt32(Console.ReadLine());
Console.Write("Zone type: \n");
string type = Console.ReadLine();
using (StreamReader sr = new StreamReader("cert.txt"))
{
	cert = sr.ReadToEnd();               
}
using (StreamReader sr = new StreamReader("key.txt"))
{
	key = sr.ReadToEnd();
}
var dat = "";
cert = "-----BEGIN CERTIFICATE-----\n" + cert + "\n-----END CERTIFICATE-----\n";
key = "-----BEGIN RSA PRIVATE KEY-----\n" + key + "\n-----END RSA PRIVATE KEY-----\n";

api.Post("/zones/" + type + "/" + zoneId + "/ssl.json", dat="ssl_crt=" + cert + "&ssl_key=" + key);
</pre>
  </div>
  <div class="tab-pane" id="response62">
    <pre>
{
  "code":201,
  "data":{
    "ssl":{
      "id":1459,
      "ssl_crt":"-----BEGIN CERTIFICATE-----\n{ ... your certificate ... }\n-----END CERTIFICATE-----\n",
      "ssl_cabundle":null,
      "date_expiration":"2014-01-24",
      "anycast_ip_id":null,
      "wildcard":1,
      "domain":"*.idcreator.com"
    }
  }
}
</pre>
  </div>
</div>


## Update Zone's SSL Information

Update the SSL certificate for the specified {zone_type} and
{zone_id}.

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/{zone_type}/{zone_id}/ssl.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`ssl_id`  | - | digit | id of previously created certificate (NOTE: This will become required in future revisions)
`ssl_crt` | - | <span class="label important">required</span><br /> | The SSL certificate you are installing. |
`ssl_key` | - | <span class="label important">required</span><br /> | The key for the SSL certificate you are installing. |
`ssl_cabundle` | - | The CABundle for the SSL Certificate you are installing. |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The SSL Certificate ID. |
`ssl_crt` | The SSL certificate. |
`ssl_cabundle` | The CA Bundle for the certificate. |
`domain` | The domain applicable to this certificate. |
`date_expiration` | The date of expiration for the certificate. |
`wildcard` | Flag to signify whether this is a wildcard certificate. |

### Code Samples

<ul class="nav nav-tabs" id="myTab63">
  <li class="active"><a href="#ruby63" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python63" data-toggle='tab'>Python</a></li>
  <li><a href="#perl63" data-toggle='tab'>Perl</a></li>
  <li><a href="#php63" data-toggle='tab'>PHP</a></li>
  <li><a href="#node63" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp63" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response63" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby63">
    <pre>
id = '96061'
type = 'pull'
ssl_crt = "-----BEGIN CERTIFICATE-----\n{ ... your certificate ... }\n-----END CERTIFICATE-----\n"
ssl_key = "-----BEGIN RSA PRIVATE KEY-----\n{ ... your key ... }\n-----END RSA PRIVATE KEY-----"
params = {"ssl_crt"=> ssl_crt,"ssl_key"=> ssl_key}
api.put('/zones/'+type+'/'+id+'/ssl.json',params)</pre>
  </div>
  <div class="tab-pane" id="python63">
    <pre>
id = '96061'
type = 'pull'
ssl_crt = "-----BEGIN CERTIFICATE-----\n{ ... your certificate ... }\n-----END CERTIFICATE-----\n"
ssl_key = "-----BEGIN RSA PRIVATE KEY-----\n{ ... your key ... }\n-----END RSA PRIVATE KEY-----"
params = {"ssl_crt": ssl_crt,"ssl_key": ssl_key}
api.put('/zones/'+type+'/'+id+'/ssl.json',params)</pre>
  </div>
    <div class="tab-pane" id="perl63">
    <pre>
my $id = 236828;
my $type = "pull";
my @params = ('ssl_crt=-----BEGIN CERTIFICATE-----\n{ ... your certificate ... }\n-----END CERTIFICATE-----\n', 'ssl_key=-----BEGIN RSA PRIVATE KEY-----\n{ ... your key ... }\n-----END RSA PRIVATE KEY-----');
$api->put("/zones/" . $type . "/" . $id . "/ssl.json", @params);</pre>
  </div>
  <div class="tab-pane" id="php63">
    <pre>
$id = '96061';
$type = 'pull';
$ssl_crt = "-----BEGIN CERTIFICATE-----\n{ ... your certificate ... }\n-----END CERTIFICATE-----\n";
$ssl_key = "-----BEGIN RSA PRIVATE KEY-----\n{ ... your key ... }\n-----END RSA PRIVATE KEY-----";
$params = array("ssl_crt"=>$ssl_crt,"ssl_key"=>$ssl_key);
$api->put('/zones/'.$type.'/'.$id.'/ssl.json',$params);</pre>
  </div>
  <div class="tab-pane" id="node63">
  <pre>
var id = '96061'
var type = 'pull'
var ssl_crt = "-----BEGIN CERTIFICATE-----\n{ ... your certificate ... }\n-----END CERTIFICATE-----\n"
var ssl_key = "-----BEGIN RSA PRIVATE KEY-----\n{ ... your key ... }\n-----END RSA PRIVATE KEY-----"
api.put('/zones/' + type + '/' + id + '/ssl.json', { ssl_crt: ssl_crt, ssl_key: ssl_key }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
    <div class="tab-pane" id="csharp63">
  <pre>
var cert = "";
var key = "";
Console.Write("Zone id: \n");
int zoneId = Convert.ToInt32(Console.ReadLine());
Console.Write("Zone type: \n");
string type = Console.ReadLine();
using (StreamReader sr = new StreamReader("cert.txt"))
{
	cert = sr.ReadToEnd();               
}
using (StreamReader sr = new StreamReader("key.txt"))
{
	key = sr.ReadToEnd();
}
var dat = "";
cert = "-----BEGIN CERTIFICATE-----\n" + cert + "\n-----END CERTIFICATE-----\n";
key = "-----BEGIN RSA PRIVATE KEY-----\n" + key + "\n-----END RSA PRIVATE KEY-----\n";

api.Put("/zones/" + type + "/" + zoneId + "/ssl.json", dat="ssl_crt=" + cert + "&ssl_key=" + key);
</pre>
  </div>
  <div class="tab-pane" id="response63">
    <pre>
{
  "code":201,
  "data":{
    "ssl":{
      "id":1459,
      "ssl_crt":"-----BEGIN CERTIFICATE-----\n{ ... your certificate ... }\n-----END CERTIFICATE-----\n",
      "ssl_cabundle":null,
      "date_expiration":"2014-01-24",
      "anycast_ip_id":null,
      "wildcard":1,
      "domain":"*.idcreator.com"
    }
  }
}
</pre>
  </div>
</div>


## Remove Zone's SSL Information

Remove the SSL certificate for the specified {zone_type} and
{zone_id}.

<div class="heading">
<div class="url DELETE"><span class="http_method">DELETE</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/{zone_type}/{zone_id}/ssl.json</span></div>
</div>


### Code Samples

<ul class="nav nav-tabs" id="myTab64">
  <li class="active"><a href="#ruby64" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python64" data-toggle='tab'>Python</a></li>
  <li><a href="#perl64" data-toggle='tab'>Perl</a></li>
  <li><a href="#php64" data-toggle='tab'>PHP</a></li>
  <li><a href="#node64" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp64" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response64" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby64">
    <pre>
id = '96061'
type = 'pull'
api.delete('/zones/'+type+'/'+id+'/ssl.json')</pre>
  </div>
  <div class="tab-pane" id="python64">
    <pre>
id = '96061'
type = 'pull'
api.delete('/zones/'+type+'/'+id+'/ssl.json')</pre>
  </div>
    <div class="tab-pane" id="perl64">
    <pre>
my $id = 236828;
my $type = "pull";
$api->delete("/zones/" . $type . "/" . $id . "/ssl.json");</pre>
  </div>
  <div class="tab-pane" id="php64">
    <pre>
$id = '96061';
$type = 'pull';
$api->delete('/zones/'.$type.'/'.$id.'/ssl.json');</pre>
  </div>
  <div class="tab-pane" id="node64">
  <pre>
var id = '96061'
var type = 'pull'
api.delete('/zones/' + type + '/' + id + '/ssl.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp64">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Zone type: \n");
string type = Console.ReadLine();

api.Delete("/zones/" + type + "/" + zoneID + "/ssl.json");
</pre>
  </div>
  <div class="tab-pane" id="response64">
    <pre>
{
  "code":200,
  "data":{
    "zone":{
      "id":"90652",
      "name":"newpullzonec5",
      "username":"username",
      "company_id":"1234",
      "url":"http:\/\/someplace.net",
      "port":"80",
      "ip":"123.0.0.49",
      "vhost":"someplace.net",
      "type":"2",
      "compress":"0",
      "backend_compress":"0",
      "queries":"1",
      "max_cache_size":"50000",
      "suspend":"0",
      "cache_valid":"1d",
      "content_encoding":"1",
      "label":"",
      "inactive":"0",
      "valid_referers":null,
      "key_zone_size":"50m",
      "expires":null,
      "disallow_robots":"0",
      "disallow_robots_txt":null,
      "canonical_link_headers":"0",
      "content_disposition":"0",
      "custom_domain_limit":"7",
      "locked":"0",
      "server_id":"123",
      "ssl":0,
      "sslshared":"0",
      "creation_date":"2013-07-22 19:00:54",
      "dsa_ip":null,
      "geo_enabled":"0",
      "set_host_header":null,
      "ssl_id":0,
      "dns_check":"1",
      "hit_bandwidth_by_dir":"0",
      "hit_bandwidth_by_custom_domain":"0",
      "hit_bandwidth_by_file_name_status_code":"0",
      "cache_version":"0",
      "ignore_setcookie_header":"0",
      "hide_setcookie_header":"0",
      "ignore_cache_control":"0",
      "use_stale":"0",
      "proxy_cache_lock":"0",
      "pseudo_streaming":"0",
      "secret":null,
      "upstream_enabled":"0",
      "cdn_url":"newpullzonec5.username.netdna-cdn.com",
      "tmp_url":"newpullzonec5.nycacorp.netdna-cdn.com"
    }
  }
}
</pre>
  </div>
</div>


# Zones Upstream API

## Get Upstream information for the current zone

Get the upstream information for the specified {zone_id}.

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/{zone_type}/{zone_id}/upstream.json</span></div>
</div>

### Code Samples

<ul class="nav nav-tabs" id="myTab65">
  <li class="active"><a href="#ruby65" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python65" data-toggle='tab'>Python</a></li>
  <li><a href="#perl65" data-toggle='tab'>Perl</a></li>
  <li><a href="#php65" data-toggle='tab'>PHP</a></li>
  <li><a href="#node65" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp65" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response65" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby65">
    <pre>
type = 'pull'
id = '96061'
api.get('/zones/'+type+'/'+id+'/upstream.json')</pre>
  </div>
  <div class="tab-pane" id="python65">
    <pre>
type = 'pull'
id = '96061'
api.get('/zones/'+type+'/'+id+'/upstream.json')</pre>
  </div>
    <div class="tab-pane" id="perl65">
    <pre>
my $id = 236828;
my $type = "pull";
$api->get("/zones/" . $type . "/" . $id . "/upstream.json");</pre>
  </div>
  <div class="tab-pane" id="php65">
    <pre>
$type = 'pull';
$id = '96061';
$api->get('/zones/'.$type.'/'.$id.'/upstream.json');</pre>
  </div>
  <div class="tab-pane" id="node65">
  <pre>
var type = 'pull'
var id = '96061'
api.get('/zones/' + type + '/' + id + '/upstream.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp65">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Zone type: \n");
string type = Console.ReadLine();

api.Get("/zones/" + type + "/" + zoneID + "/upstream.json");
</pre>
  </div>
  <div class="tab-pane" id="response65">
    <pre>
{u'code': 200, u'data': {u'total': 1, u'upstreams': [{u'weight': u'1', u'id': u'121', u'bucket_id': u'96061', u'server': u'http://cdn.somedomain.com', u'backup': u'0', u'port': u'80'}]}}
</pre>
  </div>
</div>


## Enable Upstream on Zone

Create and enable Upstream for a specific {zone_id}.

<div class="heading">
<div class="url POST"><span class="http_method">POST</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/{zone_type}/{zone_id}/upstream.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`server` | - | <span class="label important">required</span><br /> | The server URL or IP to provide the streaming resources
`port` | - | <span class="label important">required</span><br /> | The port where server is to be called


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The Upstream ID.
`bucket_id` | The bucket_id it belongs to
`server` | The server URL or IP
`port` | The port it uses to call the server

### Code Samples

<ul class="nav nav-tabs" id="myTab66">
  <li class="active"><a href="#ruby66" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python66" data-toggle='tab'>Python</a></li>
  <li><a href="#perl66" data-toggle='tab'>Perl</a></li>
  <li><a href="#php66" data-toggle='tab'>PHP</a></li>
  <li><a href="#node66" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp66" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response66" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby66">
    <pre>
type = 'pull'
id = '96061'
params = {"server"=> "http://cdn.somedomain.com","port"=> "80"}
api.post('/zones/'+type+'/'+id+'/upstream.json', params)</pre>
  </div>
  <div class="tab-pane" id="python66">
    <pre>
type = 'pull'
id = '96061'
params = {"server": "http://cdn.somedomain.com","port": "80"}
api.post('/zones/'+type+'/'+id+'/upstream.json', params)</pre>
  </div>
    <div class="tab-pane" id="perl66">
    <pre>
my $id = 96061;
my $type = "pull";
my @params = {server => 'http://cdn.somedomain.com', port => '80'};
$api->post("/zones/" . $type . "/" . $id . "/upstream.json", @params);</pre>
  </div>
  <div class="tab-pane" id="php66">
    <pre>
$type = 'pull';
$id = '96061';
$params = array("server"=>"http://cdn.somedomain.com","port"=>"80");
$api->post('/zones/'.$type.'/'.$id.'/upstream.json', $params);</pre>
  </div>
  <div class="tab-pane" id="node66">
  <pre>
var type = 'pull'
var id = '96061'
api.post('/zones/' + type + '/' + id + '/upstream.json', {server: 'http://cdn.somedomain.com', port: '80' }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp66">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Zone type: \n");
string type = Console.ReadLine();

api.Post("/zones/" + type + "/" + zoneID + "/upstream.json", "server=http://cdn.somedomain.com&port=80");
</pre>
  </div>
  <div class="tab-pane" id="response66">
    <pre>
</pre>
  </div>
</div>


## Update Zone's Upstream Information

Update the Upstream information for the specified {zone_id}.

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/{zone_type}/{zone_id}/upstream.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`upstream_id` | - | <span class="label important">required</span><br /> | The Upstream Information you're modifying
`server` | - | <span class="label important">required</span><br /> | The server URL or IP
`port` | - | <span class="label important">required</span><br /> | The port used to call the server


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The Upstream ID.
`bucket_id` | The bucket_id it belongs to
`server` | The server URL or IP
`port` | The port it uses to call the server

### Code Samples

<ul class="nav nav-tabs" id="myTab67">
  <li class="active"><a href="#ruby67" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python67" data-toggle='tab'>Python</a></li>
  <li><a href="#perl67" data-toggle='tab'>Perl</a></li>
  <li><a href="#php67" data-toggle='tab'>PHP</a></li>
  <li><a href="#node67" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp67" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response67" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby67">
    <pre>
type = 'pull'
id = '96061'
upstream_id = '123'
params = {"upstream_id"=> "93013","server"=> "http://somedomain.com","port"=> "80"}
api.put('/zones/'+type+'/'+id+'/upstream.json/'+upstream_id, params)</pre>
  </div>
  <div class="tab-pane" id="python67">
    <pre>
type = 'pull'
id = '96061'
upstream_id = '123'
params = {"upstream_id": "93013","server": "http://somedomain.net","port": "80"}
api.put('/zones/'+type+'/'+id+'/upstream.json/'+upstream_id, params)</pre>
  </div>
    <div class="tab-pane" id="perl67">
    <pre>
my $id = 96061;
my $type = "pull";
my $upstream_id = "123";
my @params = ('upstream_id=93013', 'server=http://somedomain.net', 'port=80');
$api->put("/zones/" . $type . "/" . $id . "/upstream.json/" . $upstream_id, @params);</pre>
  </div>
  <div class="tab-pane" id="php67">
    <pre>
$type = 'pull';
$id = '96061';
$upstream_id = '123';
$params = array("upstream_id"=>"93013","server"=>"http://somedomain.net","port"=>"80");
$api->put('/zones/' . $type . '/' . $id . '/upstream.json/' . $upstream_id, $params);</pre>
  </div>
  <div class="tab-pane" id="node67">
  <pre>
var type = 'pull'
var id = '96061'
var upstream_id = '123'
api.put('/zones/' + type + '/' + id + '/upstream.json/' + upstream_id, { upstream_id: '93013', server: 'http://somedomain.net', port: '80' }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp67">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Zone type: \n");
string type = Console.ReadLine();
Console.Write("Upstream ID: \n");
int upstreamID = Convert.ToInt32(Console.ReadLine());
Console.Write("Upstream ID: \n");
int upstream_id = Convert.ToInt32(Console.ReadLine());

api.Put("/zones/" + type + "/" + zoneID + "/upstream.json/" + upstream_id, "upstream_id=" + upstreamID + "&server=http://somedomain.com&port=80");
</pre>
  </div>
  <div class="tab-pane" id="response67">
    <pre>
</pre>
  </div>
</div>


## Remove Zone's Upstream Information

Remove the Upstream Information for the specified {zone_id}.

<div class="heading">
<div class="url DELETE"><span class="http_method">DELETE</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/zones/{zone_type}/{zone_id}/upstream.json</span></div>
</div>


### Code Samples

<ul class="nav nav-tabs" id="myTab68">
  <li class="active"><a href="#ruby68" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python68" data-toggle='tab'>Python</a></li>
  <li><a href="#perl68" data-toggle='tab'>Perl</a></li>
  <li><a href="#php68" data-toggle='tab'>PHP</a></li>
  <li><a href="#node68" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp68" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response68" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby68">
    <pre>
type = 'pull'
id = '96061'
upstream_id = '123'
api.delete('/zones/'+type+'/'+id+'/upstream.json/'+upstream_id)</pre>
  </div>
  <div class="tab-pane" id="python68">
    <pre>
type = 'pull'
id = '96061'
upstream_id = '123'
api.delete('/zones/'+type+'/'+id+'/upstream.json/'+upstream_id)</pre>
  </div>
    <div class="tab-pane" id="perl68">
    <pre>
my $id = 96061;
my $type = "pull";
my $upstream_id = "123";
$api->delete("/zones/" . $type . "/" . $id . "/upstream.json/" . $upstream_id);</pre>
  </div>
  <div class="tab-pane" id="php68">
    <pre>
$type = 'pull';
$id = '96061';
$upstream_id = '123';
$api->delete('/zones/' . $type . '/' . $id . '/upstream.json/' . $upstream_id);</pre>
  </div>
  <div class="tab-pane" id="node68">
  <pre>
var type = 'pull'
var id = '96061'
var upstream_id = '123'
api.delete('/zones/' + type + '/' + id + '/upstream.json/' + upstream_id, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp68">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Zone type: \n");
string type = Console.ReadLine();
Console.Write("Upstream ID: \n");
int upstream_id = Convert.ToInt32(Console.ReadLine());

api.Delete("/zones/" + type + "/" + zoneID + "/upstream.json/" + upstream_id);
</pre>
  </div>
  <div class="tab-pane" id="response68">
    <pre>
</pre>
  </div>
</div>


