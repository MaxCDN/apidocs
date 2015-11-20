# Reports API

## Get Account Stats

Gets the total usage statistics for your account, optionally broken up by
{report_type}. If no {report_type} is given the request will return
the total usage on your account.

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/stats.json/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01) | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-01) | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`size` | The amount of bytes transferred |
`hit` | The number of times files were requested |
`noncache_hit` | The number of times a requested file was not in cache |
`cache_hit` | The number of times a requested file was already cached |
`timestamp` | The timestamp for the corresponding {report_type} |

### Code Samples

<ul class="nav nav-tabs" id="myTab69">
  <li class="active"><a href="#ruby69" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python69" data-toggle='tab'>Python</a></li>
  <li><a href="#perl69" data-toggle='tab'>Perl</a></li>
  <li><a href="#php69" data-toggle='tab'>PHP</a></li>
  <li><a href="#node69" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp69" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response69" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby69">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/stats.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python69">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/stats.json'+reportType)</pre>

  </div>
    <div class="tab-pane" id="perl69">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
$api->get("/reports/stats.json" . $reportType);</pre>
<
  </div>
  <div class="tab-pane" id="php69">
    <pre>
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$api->get('/reports/stats.json/'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node69">
  <pre>
var reportType = '' //Vaild input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/stats.json/' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp69">
  <pre>
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();

api.Get("/reports/stats.json" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response69">
    <pre>
{
    "code": 200,
    "data": {
        "stats": {
            "cache_hit": "0",
            "hit": "20",
            "noncache_hit": "20",
            "size": "0"
        },
        "total": "1"
    }
}</pre>
  </div>
</div>


## Get All Zone Stats

Gets the total usage statistics for each of your zones, optionally broken up by
{report_type}. If no {report_type} is given the timestamp response parameter will be omitted.

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/statsbyzone.json/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01) | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-01) | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`bucket_id` | The Zone ID that corresponds to this set of stats |
`size` | The amount of bytes transferred |
`hit` | The number of times files were requested |
`noncache_hit` | The number of times a requested file was not in cache |
`cache_hit` | The number of times a requested file was already cached |
`timestamp` | The timestamp for the corresponding {report_type} |

### Code Samples

<ul class="nav nav-tabs" id="myTab100">
  <li class="active"><a href="#ruby100" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python100" data-toggle='tab'>Python</a></li>
  <li><a href="#perl100" data-toggle='tab'>Perl</a></li>
  <li><a href="#php100" data-toggle='tab'>PHP</a></li>
  <li><a href="#node100" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp100" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response100" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby100">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/statsbyzone.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python100">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/statsbyzone.json'+reportType)</pre>

  </div>
    <div class="tab-pane" id="perl100">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
$api->get("/reports/statsbyzone.json" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php100">
    <pre>
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$api->get('/reports/statsbyzone.json/'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node100">
  <pre>
var reportType = '' //Vaild input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/statsbyzone.json/' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp100">
  <pre>
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();

api.Get("/reports/statsbyzone.json" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response100">
    <pre>
{
  "code": 200,
  "data": {
    "page": 1,
    "pages": 262,
    "page_size": 50,
    "current_page_size": 50,
    "total": 13097,
    "stats": [
      {
        "zone_id": "4816",
        "size": "20318527",
        "hit": "280",
        "cache_hit": "15",
        "noncache_hit": "265"
      },
      {
        "zone_id": "5023",
        "size": "18032138",
        "hit": "119120",
        "cache_hit": "0",
        "noncache_hit": "119120"
      },
      {
        "zone_id": "5045",
        "size": "10656749286",
        "hit": "950640",
        "cache_hit": "838432",
        "noncache_hit": "112208"
      },

      ....

    ],
    "summary": {
      "size": 5.7138288549144e+14,
      "hit": 17093013874,
      "cache_hit": 14815205275,
      "noncache_hit": 2277808599
    }
  }
}</pre>
  </div>
</div>


## Get a Zone's Stats

Gets the {zone_id} usage statistics optionally broken up by
{report_type}. If no {report_type} is given the request will return
the total usage for the zones.

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/{zone_id}/stats.json/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01) | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-01) | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`size` | The amount of bytes transferred |
`hit` | The number of times files were requested |
`noncache_hit` | The number of times a requested file was not in cache |
`cache_hit` | The number of times a requested file was already cached |
`timestamp` | The timestamp for the corresponding {report_type} |



### Code Samples

<ul class="nav nav-tabs" id="myTab70">
  <li class="active"><a href="#ruby70" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python70" data-toggle='tab'>Python</a></li>
  <li><a href="#perl70" data-toggle='tab'>Perl</a></li>
  <li><a href="#php70" data-toggle='tab'>PHP</a></li>
  <li><a href="#node70" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp70" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response70" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby70">
    <pre>
id = '96061'
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/'+id+'/stats.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python70">
    <pre>
id = '96061'
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/'+id+'/stats.json'+reportType)</pre>

  </div>
    <div class="tab-pane" id="perl70">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
my $id = 96061;
$api->get("/reports/" . $id . "/stats.json" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php70">
    <pre>
$id = '96061';
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$api->get('/reports/'.$id.'/stats.json/'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node70">
  <pre>
var id = '96061'
var reportType = '' //Vaild input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/' + id + '/stats.json/' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp70">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();

api.Get("/reports/" + zoneID + "/stats.json" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response70">
    <pre>
{
    "code": 200,
    "data": {
        "stats": {
            "cache_hit": null,
            "hit": null,
            "noncache_hit": null,
            "size": null
        },
        "summary": {
            "cache_hit": null,
            "hit": null,
            "noncache_hit": null,
            "size": null
        },
        "total": "0"
    }
}</pre>
  </div>
</div>


# Reports by Location API

## List Nodes

Gets a list of all active nodes (locations)

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/nodes.json</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | Node Id |
`name` | Node 3 letter code |
`description` | Full node name |

### Code Samples

<ul class="nav nav-tabs" id="myTab71">
  <li class="active"><a href="#ruby71" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python71" data-toggle='tab'>Python</a></li>
  <li><a href="#perl71" data-toggle='tab'>Perl</a></li>
  <li><a href="#php71" data-toggle='tab'>PHP</a></li>
  <li><a href="#node71" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp71" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response71" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby71">
    <pre>
api.get('/reports/nodes.json')</pre>

  </div>
  <div class="tab-pane" id="python71">
    <pre>
api.get('/reports/nodes.json')</pre>

  </div>
    <div class="tab-pane" id="perl71">
    <pre>
$api->get("/reports/nodes.json")</pre>

  </div>
  <div class="tab-pane" id="php71">
    <pre>
$api->get('/reports/nodes.json');</pre>

  </div>
  <div class="tab-pane" id="node71">
  <pre>
api.get('/reports/nodes.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp71">
  <pre>
api.Get("/reports/nodes.json");
</pre>

  </div>
  <div class="tab-pane" id="response71">
    <pre>
{
    "code": 200,
    "data": {
        "nodes": [
            {
                "description": "Los Angeles",
                "id": "1",
                "name": "lax"
            },
            {
                "description": "New York",
                "id": "3",
                "name": "jfk"
            },
            {
                "description": "Seattle",
                "id": "2",
                "name": "sea"
            },
            {
                "description": "Atlanta",
                "id": "4",
                "name": "atl"
            },
            {
                "description": "Amsterdam",
                "id": "5",
                "name": "ams"
            },
            {
                "description": "Dallas",
                "id": "6",
                "name": "dal"
            },
            {
                "description": "Chicago",
                "id": "8",
                "name": "chi"
            },
            {
                "description": "Virginia",
                "id": "9",
                "name": "vir"
            },
            {
                "description": "Miami",
                "id": "7",
                "name": "mia"
            },
            {
                "description": "London",
                "id": "12",
                "name": "lhr"
            },
            {
                "description": "San Francisco",
                "id": "13",
                "name": "sfo"
            },
            {
                "description": "Los Angeles 3",
                "id": "30",
                "name": "lax"
            }
        ]
    }
}</pre>
  </div>
</div>


## List Nodes by Zone

Gets a list of all active nodes (locations) specified by the
{zone_id} parameter

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/{zone_id}/nodes.json</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | Node Id |
`name` | Node 3 letter code |
`description` | Full node name |

### Code Samples

<ul class="nav nav-tabs" id="myTab72">
  <li class="active"><a href="#ruby72" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python72" data-toggle='tab'>Python</a></li>
  <li><a href="#perl72" data-toggle='tab'>Perl</a></li>
  <li><a href="#php72" data-toggle='tab'>PHP</a></li>
  <li><a href="#node72" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp72" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response72" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby72">
    <pre>
id = '96061'
api.get('/reports/'+id+'/nodes.json')</pre>

  </div>
  <div class="tab-pane" id="python72">
    <pre>
id = '96061'
api.get('/reports/'+id+'/nodes.json')</pre>

  </div>
    <div class="tab-pane" id="perl72">
    <pre>
my $id = 96061;
$api->get("/reports/" . $id . "/nodes.json");</pre>

  </div>
  <div class="tab-pane" id="php72">
    <pre>
$id = '96061';
$api->get('/reports/'.$id.'/nodes.json');</pre>

  </div>
  <div class="tab-pane" id="node72">
  <pre>
var id = '96061'
api.get('/reports/' + id + '/nodes.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp72">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());

api.Get("/reports/" + zoneID + "/nodes.json");
</pre>

  </div>
  <div class="tab-pane" id="response72">
    <pre>
{
    "code": 200,
    "data": {
        "nodes": [
            {
                "description": "Dallas",
                "id": "6",
                "name": "dal"
            },
            {
                "description": "Los Angeles",
                "id": "1",
                "name": "lax"
            },
            {
                "description": "Seattle",
                "id": "2",
                "name": "sea"
            },
            {
                "description": "New York",
                "id": "3",
                "name": "jfk"
            },
            {
                "description": "Atlanta",
                "id": "4",
                "name": "atl"
            },
            {
                "description": "Amsterdam",
                "id": "5",
                "name": "ams"
            },
            {
                "description": "Chicago",
                "id": "8",
                "name": "chi"
            },
            {
                "description": "Virginia",
                "id": "9",
                "name": "vir"
            },
            {
                "description": "London",
                "id": "12",
                "name": "lhr"
            },
            {
                "description": "San Francisco",
                "id": "13",
                "name": "sfo"
            }
        ]
    }
}</pre>
  </div>
</div>


## List Zone Node Stats by Report Type

Get usage statistics broken up by nodes and optionally
{report_type}. If no {report_type} is given the request will return
the total usage broken up by node.

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/nodes.json/stats/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-31) | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-31) | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`pop_id` | Node Id |
`pop_name` | Node 3 letter code, only returned when {report_type} is not empty |
`pop_description` | Full node name, only returned when {report_type} is not empty |
`size` | The amount of bytes transferred |
`hit` | The number of times files were requested |
`noncache_hit` | The number of times a requested file was not in cache |
`cache_hit` | The number of times a requested file was already cached |
`timestamp` | A timestamp corresponding to {report_type}, only returned when {report_type} is not empty |

### Code Samples

<ul class="nav nav-tabs" id="myTab73">
  <li class="active"><a href="#ruby73" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python73" data-toggle='tab'>Python</a></li>
  <li><a href="#perl73" data-toggle='tab'>Perl</a></li>
  <li><a href="#php73" data-toggle='tab'>PHP</a></li>
  <li><a href="#node73" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp73" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response73" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby73">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/nodes.json/stats'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python73">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/nodes.json/stats'+reportType)</pre>

  </div>
    <div class="tab-pane" id="perl73">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
$api->get("/reports/nodes.json/stats" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php73">
    <pre>
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$api->get('/reports/nodes.json/stats/'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node73">
  <pre>
var reportType = '' //Vaild input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/nodes.json/stats/' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp73">
  <pre>
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();

api.Get("/reports/nodes.json/stats" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response73">
    <pre>
{
    "code": 200,
    "data": {
        "stats": [
            {
                "cache_hit": "0",
                "hit": "2",
                "noncache_hit": "2",
                "pop_description": "Los Angeles",
                "pop_id": "1",
                "pop_name": "lax",
                "size": "0"
            },
            {
                "cache_hit": "0",
                "hit": "2",
                "noncache_hit": "2",
                "pop_description": "Atlanta",
                "pop_id": "4",
                "pop_name": "atl",
                "size": "0"
            },
            {
                "cache_hit": "0",
                "hit": "2",
                "noncache_hit": "2",
                "pop_description": "Chicago",
                "pop_id": "8",
                "pop_name": "chi",
                "size": "0"
            },
            {
                "cache_hit": "0",
                "hit": "2",
                "noncache_hit": "2",
                "pop_description": "San Francisco",
                "pop_id": "13",
                "pop_name": "sfo",
                "size": "0"
            },
            {
                "cache_hit": "0",
                "hit": "2",
                "noncache_hit": "2",
                "pop_description": "Seattle",
                "pop_id": "2",
                "pop_name": "sea",
                "size": "0"
            },
            {
                "cache_hit": "0",
                "hit": "2",
                "noncache_hit": "2",
                "pop_description": "Amsterdam",
                "pop_id": "5",
                "pop_name": "ams",
                "size": "0"
            },
            {
                "cache_hit": "0",
                "hit": "2",
                "noncache_hit": "2",
                "pop_description": "Virginia",
                "pop_id": "9",
                "pop_name": "vir",
                "size": "0"
            },
            {
                "cache_hit": "0",
                "hit": "2",
                "noncache_hit": "2",
                "pop_description": "New York",
                "pop_id": "3",
                "pop_name": "jfk",
                "size": "0"
            },
            {
                "cache_hit": "0",
                "hit": "2",
                "noncache_hit": "2",
                "pop_description": "Dallas",
                "pop_id": "6",
                "pop_name": "dal",
                "size": "0"
            },
            {
                "cache_hit": "0",
                "hit": "2",
                "noncache_hit": "2",
                "pop_description": "London",
                "pop_id": "12",
                "pop_name": "lhr",
                "size": "0"
            }
        ],
        "summary": {
            "cache_hit": "0",
            "hit": "20",
            "noncache_hit": "20",
            "size": "0"
        },
        "total": "1"
    }
}</pre>
  </div>
</div>


## List Node Stats by Zone and Report Type

Get usage statistics for a particular {zone_id} broken up by
nodes and optionally {report_type}. If no {report_type} is given
the request will return the total usage broken up by node.

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/{zone_id}/nodes.json/stats/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01) | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-01) | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`pop_id` | Node Id |
`pop_name` | Node 3 letter code, only returned when {report_type} is not empty |
`pop_description` | Full node name, only returned when {report_type} is not empty |
`size` | The amount of bytes transferred |
`hit` | The number of times files were requested |
`noncache_hit` | The number of times a requested file was not in cache |
`cache_hit` | The number of times a requested file was already cached |
`timestamp` | A timestamp corresponding to {report_type}, only returned when {report_type} is not empty |

### Code Samples

<ul class="nav nav-tabs" id="myTab74">
  <li class="active"><a href="#ruby74" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python74" data-toggle='tab'>Python</a></li>
  <li><a href="#perl74" data-toggle='tab'>Perl</a></li>
  <li><a href="#php74" data-toggle='tab'>PHP</a></li>
  <li><a href="#node74" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp74" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response74" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby74">
    <pre>
id = '96061'
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/'+id+'/nodes.json/stats'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python74">
    <pre>
id = '96061'
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/'+id+'/nodes.json/stats'+reportType)</pre>

  </div>
    <div class="tab-pane" id="perl74">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
my $id = 96061;
$api->get("/reports/" . $id . "/nodes.json/stats" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php74">
    <pre>
$id = '96061';
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$api->get('/reports/'.$id.'/nodes.json/stats/'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node74">
  <pre>
var id = '96061'
var reportType = '' //Vaild input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/' + id + '/nodes.json/stats/' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp74">
  <pre>
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();

api.Get("/reports/" + zoneID + "/nodes.json/stats" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response74">
    <pre>
{
    "code": 200,
    "data": {
        "stats": [],
        "summary": {
            "cache_hit": null,
            "hit": null,
            "noncache_hit": null,
            "size": null
        },
        "total": null
    }
}</pre>
  </div>
</div>


## Get Zone Node

Gets the node information for the specified {node_id}

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/nodes.json/{node_id}</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | Node Id |
`name` | Node 3 letter code |
`description` | Full node name |

### Code Samples

<ul class="nav nav-tabs" id="myTab75">
  <li class="active"><a href="#ruby75" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python75" data-toggle='tab'>Python</a></li>
  <li><a href="#perl75" data-toggle='tab'>Perl</a></li>
  <li><a href="#php75" data-toggle='tab'>PHP</a></li>
  <li><a href="#node75" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp75" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response75" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby75">
    <pre>
id = '1'
api.get('/reports/nodes.json/'+id)</pre>

  </div>
  <div class="tab-pane" id="python75">
    <pre>
id = '1'
api.get('/reports/nodes.json/'+id)</pre>

  </div>
    <div class="tab-pane" id="perl75">
    <pre>
my $id = 1;
$api->get("/reports/nodes.json/" . $id);</pre>

  </div>
  <div class="tab-pane" id="php75">
    <pre>
$id = '1';
$api->get('/reports/nodes.json/'.$id);</pre>

  </div>
  <div class="tab-pane" id="node75">
  <pre>
var id = '1'
api.get('/reports/nodes.json/' + id, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp75">
  <pre>
Console.Write("Node ID: \n");
int nodeID = Convert.ToInt32(Console.ReadLine());

api.Get("/reports/nodes.json/" + nodeID);
</pre>

  </div>
  <div class="tab-pane" id="response75">
    <pre>
{
    "code": 200,
    "data": {
        "node": {
            "description": "Los Angeles",
            "id": "1",
            "name": "lax"
        }
    }
}
</pre>
  </div>
</div>


## Get Node by Zone

Gets the node information for the specified {node_id} and
{zone_id}

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/{zone_id}/nodes.json/{node_id}</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | Node Id |
`name` | Node 3 letter code |
`description` | Full node name |

### Code Samples

<ul class="nav nav-tabs" id="myTab76">
  <li class="active"><a href="#ruby76" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python76" data-toggle='tab'>Python</a></li>
  <li><a href="#perl76" data-toggle='tab'>Perl</a></li>
  <li><a href="#php76" data-toggle='tab'>PHP</a></li>
  <li><a href="#node76" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp76" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response76" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby76">
    <pre>
zoneId = '96061'
nodeId = '1'
api.get('/reports/'+zoneId+'/nodes.json/'+nodeId)</pre>

  </div>
  <div class="tab-pane" id="python76">
    <pre>
zoneId = '96061'
nodeId = '1'
api.get('/reports/'+zoneId+'/nodes.json/'+nodeId)</pre>

  </div>
    <div class="tab-pane" id="perl76">
    <pre>
my $zoneId = 96061;
my $nodeId = 1;
$api->get("/reports/" . $zoneId . "/nodes.json/" . $nodeId);</pre>

  </div>
  <div class="tab-pane" id="php76">
    <pre>
$zoneId = '96061';
$nodeId = '1';
$api->get('/reports/'.$zoneId.'/nodes.json/'.$nodeId);</pre>

  </div>
  <div class="tab-pane" id="node76">
  <pre>
var zoneId = '96061'
var nodeId = '1'
api.get('/reports/' + zoneId + '/nodes.json/' + nodeId, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp76">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Node ID: \n");
int nodeID = Convert.ToInt32(Console.ReadLine());

api.Get("/reports/" + zoneID + "/nodes.json/" + nodeID);
</pre>

  </div>
  <div class="tab-pane" id="response76">
    <pre>
{
    "code": 200,
    "data": {
        "stats": [],
        "summary": {
            "cache_hit": null,
            "hit": null,
            "noncache_hit": null,
            "size": null
        },
        "total": null
    }
}</pre>
  </div>
</div>


## Get Zone Node Stats by Report Type

Get usage statistics for a particular {node_id} optionally
broken up by {report_type}. If no {report_type} is given the
request will return the total usage for the node.

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/nodes.json/{node_id}/stats/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01) | Start date. |
`date_to` | now() | Y-m-d (e.g. 2012-01-01) | End date. |


### Response Parameters

Parameter | Description |
--- | --- | ---
`size` | The amount of bytes transferred |
`hit` | The number of times files were requested |
`noncache_hit` | The number of times a requested file was not in cache |
`cache_hit` | The number of times a requested file was already cached |
`timestamp` | A timestamp corresponding to {report_type}, only returned when {report_type} is not empty |

### Code Samples

<ul class="nav nav-tabs" id="myTab77">
  <li class="active"><a href="#ruby77" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python77" data-toggle='tab'>Python</a></li>
  <li><a href="#perl77" data-toggle='tab'>Perl</a></li>
  <li><a href="#php77" data-toggle='tab'>PHP</a></li>
  <li><a href="#node77" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp77" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response77" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby77">
    <pre>
id = '1'
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/nodes.json/'+id+'/stats'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python77">
    <pre>
id = '1'
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/nodes.json/'+id+'/stats'+reportType)</pre>

  </div>
    <div class="tab-pane" id="perl77">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
my $id = 1;
$api->get("/reports/nodes.json/" . $id . "/stats" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php77">
    <pre>
$id = '1';
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$api->get('/reports/nodes.json/'.$id.'/stats/'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node77">
  <pre>
var id = '1'
var reportType = '' //Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/nodes.json/' + id + '/stats/' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp77">
  <pre>
Console.Write("Node ID: \n");
int nodeID = Convert.ToInt32(Console.ReadLine());
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();

api.Get("/reports/nodes.json/" + nodeID + "/stats" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response77">
    <pre>
{
    "code": 200,
    "data": {
        "stats": [
            {
                "cache_hit": "0",
                "hit": "2",
                "noncache_hit": "2",
                "size": "0"
            }
        ],
        "total": "1"
    }
}</pre>
  </div>
</div>


## Get Node Stats by Zone and Report Type

Get usage statistics for a particular {node_id} and {zone_id},
optionally broken up by {report_type}. If no {report_type} is given
the request will return the total usage for the node.

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/{zone_id}/nodes.json/{node_id}/stats/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01) | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-01) | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`size` | The amount of bytes transferred |
`hit` | The number of times files were requested |
`noncache_hit` | The number of times a requested file was not in cache |
`cache_hit` | The number of times a requested file was already cached |
`timestamp` | A timestamp corresponding to {report_type}, only returned when {report_type} is not empty |



### Code Samples

<ul class="nav nav-tabs" id="myTab78">
  <li class="active"><a href="#ruby78" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python78" data-toggle='tab'>Python</a></li>
  <li><a href="#perl78" data-toggle='tab'>Perl</a></li>
  <li><a href="#php78" data-toggle='tab'>PHP</a></li>
  <li><a href="#node78" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp78" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response78" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby78">
    <pre>
zoneId='96061'
nodeId='1'
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/'+zoneId+'/nodes.json/'+nodeId+'/stats'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python78">
    <pre>
zoneId='96061'
nodeId='1'
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/'+zoneId+'/nodes.json/'+nodeId+'/stats'+reportType)</pre>

  </div>
    <div class="tab-pane" id="perl78">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
my $zoneId = 96061;
my $nodeId = 1;
$api->get("/reports/" . $zoneId . "/nodes.json/" . $nodeId . "/stats" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php78">
    <pre>
$zoneId='96061';
$nodeId='1';
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$api->get('/reports/'.$zoneId.'/nodes.json/'.$nodeId.'/stats/'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node78">
  <pre>
var zoneId = '96061'
var nodeId = '1'
var reportType = '' //Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/' + zoneId + '/nodes.json/' + nodeId + '/stats/' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp78">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Node ID: \n");
int nodeID = Convert.ToInt32(Console.ReadLine());
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();

api.Get("/reports/" + zoneID + "/nodes.json/" + nodeID + "/stats" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response78">
    <pre>
{
    "code": 200,
    "data": {
        "stats": [
            {
                "cache_hit": null,
                "hit": null,
                "noncache_hit": null,
                "size": null
            }
        ],
        "total": "0"
    }
}</pre>
  </div>
</div>


# Reports by Popular Files API

## List Popular Files

Gets the most popularly requested files for your account,
grouped into daily statistics

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/popularfiles.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01). | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-01). | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`bucket_id` | The Zone ID for the popular file |
`uri` | The URI for the requested popular file |
`hit` | The number of times the file was requested |
`size` | The amount of bytes transferred for the given file |
`vhost` | The CDN URL for the corresponding zone |
`timestamp` | UTC timestamp of the request |

### Code Samples

<ul class="nav nav-tabs" id="myTab79">
  <li class="active"><a href="#ruby79" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python79" data-toggle='tab'>Python</a></li>
  <li><a href="#perl79" data-toggle='tab'>Perl</a></li>
  <li><a href="#php79" data-toggle='tab'>PHP</a></li>
  <li><a href="#node79" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp79" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response79" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby79">
    <pre>
api.get('/reports/popularfiles.json')</pre>

  </div>
  <div class="tab-pane" id="python79">
    <pre>
api.get('/reports/popularfiles.json')</pre>

  </div>
    <div class="tab-pane" id="perl79">
    <pre>
$api->get("/reports/popularfiles.json")</pre>

  </div>
  <div class="tab-pane" id="php79">
    <pre>
$api->get('/reports/popularfiles.json');</pre>

  </div>
  <div class="tab-pane" id="node79">
  <pre>
api.get('/reports/popularfiles.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp79">
  <pre>
api.Get("/reports/popularfiles.json");
</pre>

  </div>
  <div class="tab-pane" id="response79">
    <pre>
{
    "code": 200,
    "data": {
        "current_page_size": 0,
        "page": 1,
        "page_size": "50",
        "pages": 0,
        "popularfiles": [],
        "summary": {
            "hit": null,
            "size": null
        },
        "total": "0"
    }
}</pre>
  </div>
</div>


## List Popular Files By Zone Type

Gets the most popularly requested files for your account,
filtered by {zone_type} and grouped into daily statistics

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/{zone_type}/popularfiles.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01) | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-01) | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`bucket_id` | The Zone ID for the popular file |
`uri` | The URI for the requested popular file |
`hit` | The number of times the file was requested |
`size` | The amount of bytes transferred for the given file |
`vhost` | The CDN URL for the corresponding zone |
`timestamp` | UTC timestamp of the request |



### Code Samples

<ul class="nav nav-tabs" id="myTab80">
  <li class="active"><a href="#ruby80" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python80" data-toggle='tab'>Python</a></li>
  <li><a href="#perl80" data-toggle='tab'>Perl</a></li>
  <li><a href="#php80" data-toggle='tab'>PHP</a></li>
  <li><a href="#node80" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp80" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response80" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby80">
    <pre>
type='pull'
api.get('/reports/'+type+'/popularfiles.json')</pre>

  </div>
  <div class="tab-pane" id="python80">
    <pre>
type='pull'
api.get('/reports/'+type+'/popularfiles.json')</pre>

  </div>
    <div class="tab-pane" id="perl80">
    <pre>
my $type = "pull";
$api->get("/reports/" . $type . "/popularfiles.json");</pre>

  </div>
  <div class="tab-pane" id="php80">
    <pre>
$type='pull';
$api->get('/reports/'.$type.'/popularfiles.json');</pre>

  </div>
  <div class="tab-pane" id="node80">
  <pre>
var type = 'pull'
api.get('/reports/' + type + '/popularfiles.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp80">
  <pre>
Console.Write("Zone type: \n");
string type = Console.ReadLine();
	
api.Get("/reports/" + type + "/popularfiles.json");
</pre>

  </div>
  <div class="tab-pane" id="response80">
    <pre>
{
    "code": 200,
    "data": {
        "current_page_size": 0,
        "page": 1,
        "page_size": "50",
        "pages": 0,
        "popularfiles": [],
        "summary": {
            "hit": null,
            "size": null
        },
        "total": "0"
    }
}</pre>
  </div>
</div>


# Reports by Status Codes API

## List Status Code Responses

Gets HTTP status code response statistics for your account

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/statuscodes.json/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01) | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-01) | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`status_code` | The HTTP status code for the response |
`hit` | The number of responses with this status code |
`definition` | The definition for the status code |

### Code Samples

<ul class="nav nav-tabs" id="myTab81">
  <li class="active"><a href="#ruby81" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python81" data-toggle='tab'>Python</a></li>
  <li><a href="#perl81" data-toggle='tab'>Perl</a></li>
  <li><a href="#php81" data-toggle='tab'>PHP</a></li>
  <li><a href="#node81" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp81" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response81" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby81">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/statuscodes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python81">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/statuscodes.json'+reportType)</pre>

  </div>
    <div class="tab-pane" id="perl81">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
$api->get("/reports/statuscodes.json/" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php81">
    <pre>
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$api->get('/reports/statuscodes.json/'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node81">
  <pre>
var reportType = '' //Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/statuscodes.json' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp81">
  <pre>
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();

api.Get("/reports/statuscodes.json" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response81">
    <pre>
{
    "code": 200,
    "data": {
        "statuscodes": [
            {
                "definition": "Not Found",
                "hit": "20",
                "status_code": "404"
            }
        ],
        "summary": {
            "hit": "20"
        },
        "total": "1"
    }
}</pre>
  </div>
</div>


## List Status Code Responses by Zone Id

Gets HTTP status code response statistics for a specific
{zone_id}

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/{zone_id}/statuscodes.json/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01) | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-01) | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`status_code` | The HTTP status code for the response |
`hit` | The number of responses with this status code |
`definition` | The definition for the status code |

### Code Samples

<ul class="nav nav-tabs" id="myTab82">
  <li class="active"><a href="#ruby82" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python82" data-toggle='tab'>Python</a></li>
  <li><a href="#perl82" data-toggle='tab'>Perl</a></li>
  <li><a href="#php82" data-toggle='tab'>PHP</a></li>
  <li><a href="#node82" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp82" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response82" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby82">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
id = '96061'
api.get('/reports/'+id+'/statuscodes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python82">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
id = '96061'
api.get('/reports/'+id+'/statuscodes.json'+reportType)</pre>

  </div>
    <div class="tab-pane" id="perl82">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
my $id = 96061;
$api->get("/reports/" . $id . "/statuscodes.json" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php82">
    <pre>
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$id = '96061';
$api->get('/reports/'.$id.'/statuscodes.json/'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node82">
  <pre>
var reportType = '' //Valid input includes '/daily', '/hourly', '/monthly' or ''
var id = '96061'
api.get('/reports/' + id + '/statuscodes.json/' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp82">
  <pre>
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n"); 
string reportType = Console.ReadLine();
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());

api.Get("/reports/" + zoneID + "/statuscodes.json" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response82">
    <pre>
{
    "code": 200,
    "data": {
        "statuscodes": [],
        "summary": {
            "hit": null
        },
        "total": "0"
    }
}</pre>
  </div>
</div>


## List Status Codes by Zone Type

Gets HTTP status code response statistics for a specific
{zone_type}

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/{zone_type}/statuscodes.json/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01) | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-01) | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`status_code` | The HTTP status code for the response |
`hit` | The number of responses with this status code |
`definition` | The definition for the status code |

### Code Samples

<ul class="nav nav-tabs" id="myTab83">
  <li class="active"><a href="#ruby83" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python83" data-toggle='tab'>Python</a></li>
  <li><a href="#perl83" data-toggle='tab'>Perl</a></li>
  <li><a href="#php83" data-toggle='tab'>PHP</a></li>
  <li><a href="#node83" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp83" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response83" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby83">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
zoneType = 'pull'
api.get('/reports/'+zoneType+'/statuscodes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python83">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
zoneType = 'pull'
api.get('/reports/'+zoneType+'/statuscodes.json'+reportType)</pre>

  </div>
    <div class="tab-pane" id="perl83">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
my $zoneType = "pull";
$api->get("/reports/" . $zoneType . "/statuscodes.json" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php83">
    <pre>
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$zoneType = 'pull';
$api->get('/reports/'.$zoneType.'/statuscodes.json/'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node83">
  <pre>
var reportType = '' //Valid input includes '/daily', '/hourly', '/monthly' or ''
var zoneType = 'pull'
api.get('/reports/' + zoneType + '/statuscodes.json/' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp83">
  <pre>
Console.Write("Zone type: \n");
string zoneType = Console.ReadLine();
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();

api.Get("/reports/" + zoneType + "/statuscodes.json" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response83">
    <pre>
{
    "code": 200,
    "data": {
        "statuscodes": [
            {
                "definition": "Not Found",
                "hit": "20",
                "status_code": "404"
            }
        ],
        "summary": {
            "hit": "20"
        },
        "total": "1"
    }
}</pre>
  </div>
</div>


## List Status Codes by Zone Id and Zone Type

Gets HTTP status code response statistics for a specific
{zone_type} and {zone_id}

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/{zone_type}/{zone_id}/statuscodes.json/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01) | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-01) | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`status_code` | The HTTP status code for the response |
`hit` | The number of responses with this status code |
`definition` | The definition for the status code |



### Code Samples

<ul class="nav nav-tabs" id="myTab84">
  <li class="active"><a href="#ruby84" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python84" data-toggle='tab'>Python</a></li>
  <li><a href="#perl84" data-toggle='tab'>Perl</a></li>
  <li><a href="#php84" data-toggle='tab'>PHP</a></li>
  <li><a href="#node84" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp84" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response84" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby84">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
zoneType = 'pull'
id = '96061'
api.get('/reports/'+zoneType+'/'+id+'/statuscodes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python84">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
zoneType = 'pull'
id = '96061'
api.get('/reports/'+zoneType+'/'+id+'/statuscodes.json'+reportType)</pre>

  </div>
    <div class="tab-pane" id="perl84">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
my $id = 96061;
my $zoneType = "pull";
$api->get("/reports/" . $zoneType . "/" . $id . "/statuscodes.json" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php84">
    <pre>
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$zoneType = 'pull';
$id = '96061';
$api->get('/reports/'.$zoneType.'/'.$id.'/statuscodes.json/'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node84">
  <pre>
var reportType = '' //Valid input includes '/daily', '/hourly', '/monthly' or ''
var zoneType = 'pull'
var id = '96061'
api.get('/reports/' + zoneType + '/' + id + '/statuscodes.json/' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp84">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Zone type: \n");
string zoneType = Console.ReadLine();
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();

api.Get("/reports/" + zoneType + "/" + zoneID + "/statuscodes.json" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response84">
    <pre>
{
    "code": 200,
    "data": {
        "statuscodes": [],
        "summary": {
            "hit": null
        },
        "total": "0"
    }
}</pre>
  </div>
</div>


# Reports by File Types API

## List File Types

Gets file type statistics for your account

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/filetypes.json/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01) | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-01) | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`file_type` | The file type requested |
`hit` | The number of times a file of this type has been requested |

### Code Samples

<ul class="nav nav-tabs" id="myTab85">
  <li class="active"><a href="#ruby85" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python85" data-toggle='tab'>Python</a></li>
  <li><a href="#perl85" data-toggle='tab'>Perl</a></li>
  <li><a href="#php85" data-toggle='tab'>PHP</a></li>
  <li><a href="#node85" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp85" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response85" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby85">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/filetypes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python85">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/filetypes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="perl85">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
$api->get("/reports/filetypes.json" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php85">
    <pre>
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$api->get('/reports/filetypes.json'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node85">
  <pre>
var reportType = '' //Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/filetypes.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp85">
  <pre>
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();

api.Get("/reports/filetypes.json" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response85">
    <pre>
{
    "code": 200,
    "data": {
        "current_page_size": 1,
        "filetypes": [
            {
                "file_type": "txt",
                "hit": "20"
            }
        ],
        "page": 1,
        "page_size": "50",
        "pages": 1,
        "summary": {
            "hit": "20"
        },
        "total": "1"
    }
}</pre>
  </div>
</div>


## List File Types by Zone Id

Gets file type statistics for a specific {zone_id}

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/{zone_id}/filetypes.json/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d e.g. 2012-01-01 | Start date |
`date_to` | now() | Y-m-d e.g. 2012-01-01 | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`file_type` | The file type requested |
`hit` | The number of times a file of this type has been requested |

### Code Samples

<ul class="nav nav-tabs" id="myTab86">
  <li class="active"><a href="#ruby86" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python86" data-toggle='tab'>Python</a></li>
  <li><a href="#perl86" data-toggle='tab'>Perl</a></li>
  <li><a href="#php86" data-toggle='tab'>PHP</a></li>
  <li><a href="#node86" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp86" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response86" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby86">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
id = '96061'
api.get('/reports/'+id+'/filetypes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python86">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
id = '96061'
api.get('/reports/'+id+'/filetypes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="perl86">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
my $id = 96061;
$api->get("/reports/" . $id . "/filetypes.json" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php86">
    <pre>
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$id = '96061';
$api->get('/reports/'.$id.'/filetypes.json/'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node86">
  <pre>
var reportType = '' //Valid input includes '/daily', '/hourly', '/monthly' or ''
var id = '96061'
api.get('/reports/' + id + '/filetypes.json/' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp86">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();

api.Get("/reports/" + zoneID + "/filetypes.json" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response86">
    <pre>
{
    "code": 200,
    "data": {
        "current_page_size": 0,
        "filetypes": [],
        "page": 1,
        "page_size": "50",
        "pages": 0,
        "summary": {
            "hit": null
        },
        "total": "0"
    }
}</pre>
  </div>
</div>


## List File Types by Zone Type

Gets file type statistics for a specific {zone_type}

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/{zone_type}/filetypes.json/{report_type}</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`file_type` | The file type requested |
`hit` | The number of times a file of this type has been requested |

### Code Samples

<ul class="nav nav-tabs" id="myTab87">
  <li class="active"><a href="#ruby87" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python87" data-toggle='tab'>Python</a></li>
  <li><a href="#perl87" data-toggle='tab'>Perl</a></li>
  <li><a href="#php87" data-toggle='tab'>PHP</a></li>
  <li><a href="#node87" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp87" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response87" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby87">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
zoneType = 'pull'
api.get('/reports/'+zoneType+'/filetypes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python87">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
zoneType = 'pull'
api.get('/reports/'+zoneType+'/filetypes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="perl87">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
my $zoneType = "pull";
$api->get("/reports/" . $zoneType . "/filetypes.json" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php87">
    <pre>
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$zoneType = 'pull';
$api->get('/reports/'.$zoneType.'/filetypes.json'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node87">
  <pre>
var reportType = '' //Valid input includes '/daily', '/hourly', '/monthly' or ''
var zoneType = 'pull'
api.get('/reports/' + zoneType + '/filetypes.json' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp87">
  <pre>
Console.Write("Zone type: \n");
string zoneType = Console.ReadLine();
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();

api.Get("/reports/" + zoneType + "/filetypes.json" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response87">
    <pre>
{
    "code": 200,
    "data": {
        "current_page_size": 1,
        "filetypes": [
            {
                "file_type": "txt",
                "hit": "20"
            }
        ],
        "page": 1,
        "page_size": "50",
        "pages": 1,
        "summary": {
            "hit": "20"
        },
        "total": "1"
    }
}</pre>
  </div>
</div>


## List File Types by Zone Id

Gets file type statistics for a specific {zone_type} and
{zone_id}

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/{zone_type}/{zone_id}/filetypes.json/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01) | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-01) | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`file_type` | The file type requested |
`hit` | The number of times a file of this type has been requested |


### Code Samples

<ul class="nav nav-tabs" id="myTab88">
  <li class="active"><a href="#ruby88" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python88" data-toggle='tab'>Python</a></li>
  <li><a href="#perl88" data-toggle='tab'>Perl</a></li>
  <li><a href="#php88" data-toggle='tab'>PHP</a></li>
  <li><a href="#node88" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp88" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response88" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby88">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
zoneType = 'pull'
id = '96061'
api.get('/reports/'+zoneType+'/'+id+'/filetypes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python88">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
zoneType = 'pull'
id = '96061'
api.get('/reports/'+zoneType+'/'+id+'/filetypes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="perl88">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
my $zoneType = "pull";
my $id = 96061;
$api->get("/reports/" . $zoneType . "/" . $id . "/filetypes.json" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php88">
    <pre>
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$zoneType = 'pull';
$id = '96061';
$api->get('/reports/'.$zoneType.'/'.$id.'/filetypes.json/'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node88">
  <pre>
var reportType = '' //Valid input includes '/daily', '/hourly', '/monthly' or ''
var zoneType = 'pull'
var id = '96061'
api.get('/reports/' + zoneType + '/' + id + '/filetypes.json/' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp88">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Zone type: \n");
string zoneType = Console.ReadLine();
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();

api.Get("/reports/" + zoneType + "/" + zoneID + "/filetypes.json" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response88">
    <pre>
{
    "code": 200,
    "data": {
        "current_page_size": 0,
        "filetypes": [],
        "page": 1,
        "page_size": "50",
        "pages": 0,
        "summary": {
            "hit": null
        },
        "total": "0"
    }
}</pre>
  </div>
</div>


# Reports by File Size Ranges API

## List File Sizes

Gets request statistics for your account based on file size
ranges

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/filesizes.json/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01) | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-01) | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`le_10k_hits` | The number of requests for files &lt;= 10KB |
`le_50k_hits` | The number of requests for files &lt;= 50KB |
`le_100k_hits` | The number of requests for files &lt;= 100KB |
`le_500k_hits` | The number of requests for files &lt;= 500KB |
`le_1m_hits` | The number of requests for files &lt;= 1MB |
`le_10m_hits` | The number of requests for files &lt;= 10MB |
`le_100m_hits` | The number of requests for files &lt;= 100MB |
`gt_100m_hits` | The number of requests for files &gt; 100MB |

### Code Samples

<ul class="nav nav-tabs" id="myTab89">
  <li class="active"><a href="#ruby89" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python89" data-toggle='tab'>Python</a></li>
  <li><a href="#perl89" data-toggle='tab'>Perl</a></li>
  <li><a href="#php89" data-toggle='tab'>PHP</a></li>
  <li><a href="#node89" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp89" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response89" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby89">
    <pre>reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/clients/{id}/reports/filesizes.json' + reportType)</pre>

  </div>
  <div class="tab-pane" id="python89">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/filesizes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="perl89">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
$api->get("/reports/filesizes.json/" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php89">
    <pre>
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$api->get('/reports/filesizes.json/'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node89">
  <pre>
var reportType = '' //Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/filesizes.json/' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp89">
  <pre>Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();
     
api.Get("/reports/filesizes.json/" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response89">
    <pre>
{
    "code": 200,
    "data": {
        "filesizes": [
            {
                "gt_100m_hit": "0",
                "le_100k_hit": "0",
                "le_100m_hit": "0",
                "le_10k_hit": "20",
                "le_10m_hit": "0",
                "le_1m_hit": "0",
                "le_500k_hit": "0",
                "le_50k_hit": "0"
            }
        ],
        "summary": {
            "hit": "20"
        }
    }
}</pre>
  </div>
</div>


## List File Sizes by Zone Id

Gets request statistics for the specified {zone_id} based on
file size ranges

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/{zone_id}/filesizes.json/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d e.g. 2012-01-01 | Start date |
`date_to` | now() | Y-m-d e.g. 2012-01-01 | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`le_10k_hits` | The number of requests for files &lt;= 10KB |
`le_50k_hits` | The number of requests for files &lt;= 50KB |
`le_100k_hits` | The number of requests for files &lt;= 100KB |
`le_500k_hits` | The number of requests for files &lt;= 500KB |
`le_1m_hits` | The number of requests for files &lt;= 1MB |
`le_10m_hits` | The number of requests for files &lt;= 10MB |
`le_100m_hits` | The number of requests for files &lt;= 100MB |
`gt_100m_hits` | The number of requests for files &gt; 100MB |

### Code Samples

<ul class="nav nav-tabs" id="myTab90">
  <li class="active"><a href="#ruby90" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python90" data-toggle='tab'>Python</a></li>
  <li><a href="#perl90" data-toggle='tab'>Perl</a></li>
  <li><a href="#php90" data-toggle='tab'>PHP</a></li>
  <li><a href="#node90" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp90" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response90" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby90">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
id = '96061'
api.get('/reports/'+id+'/filesizes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python90">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
id = '96061'
api.get('/reports/'+id+'/filesizes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="perl90">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
my $id = 96061;
$api->get("/reports/" . $id . "/filesizes.json" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php90">
    <pre>
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$id = '96061';
$api->get('/reports/'.$id.'/filesizes.json'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node90">
  <pre>
var reportType = '' //Valid input includes '/daily', '/hourly', '/monthly' or ''
var id = '96061'
api.get('/reports/' + id + '/filesizes.json' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp90">
  <pre>Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();
     
api.Get("/reports/" + zoneID + "/filesizes.json" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response90">
    <pre>
{
    "code": 200,
    "data": {
        "filesizes": [
            {
                "gt_100m_hit": null,
                "le_100k_hit": null,
                "le_100m_hit": null,
                "le_10k_hit": null,
                "le_10m_hit": null,
                "le_1m_hit": null,
                "le_500k_hit": null,
                "le_50k_hit": null
            }
        ],
        "summary": {
            "hit": null
        }
    }
}</pre>
  </div>
</div>


## List File Sizes by Zone Type

Gets request statistics for the specified {zone_type} based on
file size ranges

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/{zone_type}/filesizes.json/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d e.g. 2012-01-01 | Start date |
`date_to` | now() | Y-m-d e.g. 2012-01-01 | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`le_10k_hits` | The number of requests for files &lt;= 10KB |
`le_50k_hits` | The number of requests for files &lt;= 50KB |
`le_100k_hits` | The number of requests for files &lt;= 100KB |
`le_500k_hits` | The number of requests for files &lt;= 500KB |
`le_1m_hits` | The number of requests for files &lt;= 1MB |
`le_10m_hits` | The number of requests for files &lt;= 10MB |
`le_100m_hits` | The number of requests for files &lt;= 100MB |
`gt_100m_hits` | The number of requests for files &gt; 100MB |

### Code Samples

<ul class="nav nav-tabs" id="myTab91">
  <li class="active"><a href="#ruby91" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python91" data-toggle='tab'>Python</a></li>
  <li><a href="#perl91" data-toggle='tab'>Perl</a></li>
  <li><a href="#php91" data-toggle='tab'>PHP</a></li>
  <li><a href="#node91" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp91" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response91" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby91">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
zoneType = 'pull'
api.get('/reports/'+zoneType+'/filesizes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python91">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
zoneType = 'pull'
api.get('/reports/'+zoneType+'/filesizes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="perl91">
    <pre>
  reportType = ''; #Valid input includes '/daily', '/hourly', '/monthly' or ''
  zoneType = 'pull';
  api.get('/reports/' . $zoneType + '/filesizes.json'+reportType);</pre>

  </div>
  <div class="tab-pane" id="php91">
    <pre>
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$zoneType = 'pull';
$api->get('/reports/'.$zoneType.'/filesizes.json'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node91">
  <pre>
var reportType = '' //Valid input includes '/daily', '/hourly', '/monthly' or ''
var zoneType = 'pull'
api.get('/reports/' + zoneType + '/filesizes.json' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp91">
  <pre>Console.Write("Zone type: \n");
string zoneType = Console.ReadLine();
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();
     
api.Get("/reports/" + zoneType + "/filesizes.json" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response91">
    <pre>
{
    "code": 200,
    "data": {
        "filesizes": [
            {
                "gt_100m_hit": "0",
                "le_100k_hit": "0",
                "le_100m_hit": "0",
                "le_10k_hit": "20",
                "le_10m_hit": "0",
                "le_1m_hit": "0",
                "le_500k_hit": "0",
                "le_50k_hit": "0"
            }
        ],
        "summary": {
            "hit": "20"
        }
    }
}</pre>
  </div>
</div>


## List File Sizes by Zone Id

Gets request statistics for the specified {zone_type} and
{zone_id} based on file size ranges

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/{zone_type}/{zone_id}/filesizes.json/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01) | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-01) | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`le_10k_hits` | The number of requests for files &lt;= 10KB |
`le_50k_hits` | The number of requests for files &lt;= 50KB |
`le_100k_hits` | The number of requests for files &lt;= 100KB |
`le_500k_hits` | The number of requests for files &lt;= 500KB |
`le_1m_hits` | The number of requests for files &lt;= 1MB |
`le_10m_hits` | The number of requests for files &lt;= 10MB |
`le_100m_hits` | The number of requests for files &lt;= 100MB |
`gt_100m_hits` | The number of requests for files &gt; 100MB |


### Code Samples

<ul class="nav nav-tabs" id="myTab92">
  <li class="active"><a href="#ruby92" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python92" data-toggle='tab'>Python</a></li>
  <li><a href="#perl92" data-toggle='tab'>Perl</a></li>
  <li><a href="#php92" data-toggle='tab'>PHP</a></li>
  <li><a href="#node92" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp92" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response92" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby92">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
zoneType = 'pull'
id = '96061'
api.get('/reports/'+zoneType+'/'+id+'/filesizes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python92">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
zoneType = 'pull'
id = '96061'
api.get('/reports/'+zoneType+'/'+id+'/filesizes.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="perl92">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
my $zoneType = "pull";
my $id = 96061;
$api->get("/reports/" . $zoneType . "/" . $id . "/filesizes.json" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php92">
    <pre>
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$zoneType = 'pull';
$id = '96061';
$api->get('/reports/'.$zoneType.'/'.$id.'/filesizes.json/'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node92">
  <pre>
var reportType = '' //Valid input includes '/daily', '/hourly', '/monthly' or ''
var zoneType = 'pull'
var id = '96061'
api.get('/reports/' + zoneType + '/' + id + '/filesizes.json/' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp92">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Zone type: \n");
string zoneType = Console.ReadLine();
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();

api.Get("/reports/" + zoneType + "/" + zoneID + "/filesizes.json" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response92">
    <pre>
{
    "code": 200,
    "data": {
        "filesizes": [
            {
                "gt_100m_hit": null,
                "le_100k_hit": null,
                "le_100m_hit": null,
                "le_10k_hit": null,
                "le_10m_hit": null,
                "le_1m_hit": null,
                "le_500k_hit": null,
                "le_50k_hit": null
            }
        ],
        "summary": {
            "hit": null
        }
    }
}</pre>
  </div>
</div>


# Reports By Directory API

## List Stats By Directory

Gets usage statistics by directory for your account (this report has to be enabled by our sales department)

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/statsbydir.json/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01) | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-01) | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`bucket_id` | The Zone ID for the top level directory |
`dir` | The name of the directory |
`hit` | The number of requests made to files within this directory |
`size` | The amount of bytes transferred from within this directory |

### Code Samples

<ul class="nav nav-tabs" id="myTab93">
  <li class="active"><a href="#ruby93" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python93" data-toggle='tab'>Python</a></li>
  <li><a href="#perl93" data-toggle='tab'>Perl</a></li>
  <li><a href="#php93" data-toggle='tab'>PHP</a></li>
  <li><a href="#node93" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp93" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response93" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby93">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/statsbydir.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python93">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/statsbydir.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="perl93">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
$api->get("/reports/statsbydir.json" . $reportType);</pre>

  </div>
  <div class="tab-pane" id="php93">
    <pre>
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$api->get('/reports/statsbydir.json'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node93">
  <pre>
var reportType = '' //Valid input includes '/daily', '/hourly', '/monthly' or ''
api.get('/reports/statsbydir.json' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp93">
  <pre>
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();

api.Get("/reports/statsbydir.json" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response93">
    <pre>
{
    "code": 200,
    "data": {
        "current_page_size": 0,
        "page": 1,
        "page_size": "50",
        "pages": 0,
        "statsbydir": [],
        "summary": {
            "hit": null,
            "size": null
        },
        "total": "0"
    }
}</pre>
  </div>
</div>


## List Stats By Directory and Zone Id

Gets usage statistics by directory for the specified {zone_id} (this report has to be enabled by our sales department)

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/reports/{zone_id}/statsbydir.json/{report_type}</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`date_from` | now() - 1 month | Y-m-d (e.g. 2012-01-01) | Start date |
`date_to` | now() | Y-m-d (e.g. 2012-01-01) | End date |


### Response Parameters

Parameter | Description |
--- | --- | ---
`bucket_id` | The Zone ID for the top level directory |
`dir` | The name of the directory |
`hit` | The number of requests made to files within this directory |
`size` | The amount of bytes transferred from within this directory |


### Code Samples

<ul class="nav nav-tabs" id="myTab94">
  <li class="active"><a href="#ruby94" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python94" data-toggle='tab'>Python</a></li>
  <li><a href="#perl94" data-toggle='tab'>Perl</a></li>
  <li><a href="#php94" data-toggle='tab'>PHP</a></li>
  <li><a href="#node94" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp94" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response94" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby94">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
id = '96061'
api.get('/reports/'+id+'/statsbydir.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="python94">
    <pre>
reportType = '' #Valid input includes '/daily', '/hourly', '/monthly' or ''
id = '96061'
api.get('/reports/'+id+'/statsbydir.json'+reportType)</pre>

  </div>
  <div class="tab-pane" id="perl94">
    <pre>
my $reportType = ""; #Vaild input includes /daily, /hourly, /monthly or ""
my $id = 96061;
$api->get("/reports/" . $id . "/statsbydir.json" . $reportType);
</pre>

  </div>
  <div class="tab-pane" id="php94">
    <pre>
$reportType = ''; //Vaild input includes '/daily', '/hourly', '/monthly' or ''
$id = '96061';
$api->get('/reports/'.$id.'/statsbydir.json'.$reportType);</pre>

  </div>
  <div class="tab-pane" id="node94">
  <pre>
var reportType = '' //Valid input includes '/daily', '/hourly', '/monthly' or ''
var id = '96061'
api.get('/reports/' + id + '/' + '/statsbydir.json' + reportType, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>

  </div>
  <div class="tab-pane" id="csharp94">
  <pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());
Console.Write("Report type (/daily, /hourly, /monthly or empty string): \n");
string reportType = Console.ReadLine();

api.Get("/reports/" + zoneID + "/statsbydir.json" + reportType);
</pre>

  </div>
  <div class="tab-pane" id="response94">
    <pre>
{
    "code": 200,
    "data": {
        "current_page_size": 0,
        "page": 1,
        "page_size": "50",
        "pages": 0,
        "statsbydir": [],
        "summary": {
            "hit": null,
            "size": null
        },
        "total": "0"
    }
}</pre>
  </div>
</div>

