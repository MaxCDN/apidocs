# Origin Shield API

## Enable Origin Shield

Enable an Origin Shield on your Pull Zone

<div class="heading">
<div class="url POST"><span class="http_method">POST</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients/{id}/zones/pull/{zone_id}/zoneshields.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Description |
--- | --- | ---
`location` | Possible values: sjc for San Jose, vir for Virginia |

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The numerical ID of your request |
`zone_id` | Your Pull Zone ID |
`reporting_code` | The chosen geographical location of the Origin Shield |

### Code Samples

<ul class="nav nav-tabs" id="myTab102">
  <li class="active"><a href="#ruby102" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python102" data-toggle='tab'>Python</a></li>
  <li><a href="#perl102" data-toggle='tab'>Perl</a></li>
  <li><a href="#php102" data-toggle='tab'>PHP</a></li>
  <li><a href="#node102" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp102" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response102" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby102">
<pre>
id = '97167'
params = {"location"=>"sjc"}
api.post('/clients/{id}/zones/pull/'+id+'/zoneshields.json', params)</pre>
  </div>
  <div class="tab-pane" id="python102">
<pre>
id = '97167'
params = {"location":"sjc"}
api.post('/clients/{id}/zones/pull/'+id+'/zoneshields.json', params)</pre>
  </div>
  <div class="tab-pane" id="perl102">
<pre>
my $id = 123502;
my @params = {location => 'sjc'};
$api->post("/clients/{id}/zones/pull/" . $id . "/zoneshields.json", @params);</pre>
  </div>
  <div class="tab-pane" id="php102">
<pre>
$id = '97167';
$params = array("location"=>"sjc");
$api->post('/clients/{id}/zones/pull/'.$id.'/zoneshields.json', $params)</pre>
  </div>
  <div class="tab-pane" id="node102">
<pre>
var id = '96167'
api.post('/clients/{id}/zones/pull/' + id + '/zoneshields.json', { location: 'sjc' }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp102">
<pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());

api.Post("/clients/{id}/zones/pull/" + zoneID + "/zoneshields.json", "location=sjc");
</pre>
  </div>
  <div class="tab-pane" id="response102">
    <pre>
{
  "data": {
    "zoneshields": [
      {
        "id": 26,
        "zone_id": "97167",
        "reporting_code": "sjc",
      },
    ]
  },
  "code": 201
}</pre>
  </div>
</div>

## Update Origin Shield

Update the active Origin Shield for your Pull Zone

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients/{id}/zones/pull/{zone_id}/zoneshields.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Description |
--- | --- | ---
`location` | Possible values: sjc for San Jose, vir for Virginia |

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | The numerical ID of your request |
`zone_id` | Your Pull Zone ID |
`reporting_code` | The chosen geographical location of the Origin Shield |

### Code Samples

<ul class="nav nav-tabs" id="myTab103">
  <li class="active"><a href="#ruby103" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python103" data-toggle='tab'>Python</a></li>
  <li><a href="#perl103" data-toggle='tab'>Perl</a></li>
  <li><a href="#php103" data-toggle='tab'>PHP</a></li>
  <li><a href="#node103" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp103" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response103" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby103">
<pre>
id = '97167'
params = {"location"=>"sjc"}
api.put('/clients/{id}/zones/pull/'+id+'/zoneshields.json', params)</pre>
  </div>
  <div class="tab-pane" id="python103">
<pre>
id = '97167'
params = {"location":"sjc"}
api.put('/clients/{id}/zones/pull/'+id+'/zoneshields.json', params)</pre>
  </div>
  <div class="tab-pane" id="perl103">
<pre>
my $id = 123502;
my @params = ('location=sjc');
$api->put("/clients/{id}/zones/pull/" . $id . "/zoneshields.json", @params);</pre>
  </div>
  <div class="tab-pane" id="php103">
<pre>
$id = '97167';
$params = array("location"=>"sjc");
$api->put('/clients/{id}/zones/pull/'.$id.'/zoneshields.json', $params)</pre>
  </div>
  <div class="tab-pane" id="node103">
<pre>
var id = '96167'
api.put('/clients/{id}/zones/pull/' + id + '/zoneshields.json', { location: 'sjc' }, function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp103">
<pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());

api.Put("/clients/{id}/zones/pull/" + zoneID + "/zoneshields.json", "location=sjc");
</pre>
  </div>
  <div class="tab-pane" id="response103">
    <pre>
{
  "data": {
    "zoneshields": [
      {
        "id": 26,
        "zone_id": "97167",
        "reporting_code": "sjc",
      },
    ]
  },
  "code": 201
}</pre>
  </div>
</div>

## Delete Origin Shield

Remove the active Origin Shield from your Pull Zone

<div class="heading">
<div class="url DELETE"><span class="http_method">DELETE</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients/{id}/zones/pull/{zone_id}/zoneshields.json</span></div>
</div>

### Code Samples

<ul class="nav nav-tabs" id="myTab104">
  <li class="active"><a href="#ruby104" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python104" data-toggle='tab'>Python</a></li>
  <li><a href="#perl104" data-toggle='tab'>Perl</a></li>
  <li><a href="#php104" data-toggle='tab'>PHP</a></li>
  <li><a href="#node104" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp104" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#response104" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby104">
<pre>
id = '97167'
api.delete('/clients/{id}/zones/pull/'+id+'/zoneshields.json')</pre>
  </div>
  <div class="tab-pane" id="python104">
<pre>
id = '97167'
api.delete('/clients/{id}/zones/pull/'+id+'/zoneshields.json')</pre>
  </div>
  <div class="tab-pane" id="perl104">
<pre>
my $id = 123502;
$api->delete("/clients/{id}/zones/pull/" . $id . "/zoneshields.json");
</pre>
  </div>
  <div class="tab-pane" id="php104">
<pre>
$id = '97167';
$api->delete('/clients/{id}/zones/pull/'.$id.'/zoneshields.json')</pre>
  </div>
  <div class="tab-pane" id="node104">
<pre>
var id = '96167'
api.delete('/clients/{id}/zones/pull/' + id + '/zoneshields.json', function(err, response) {
  console.log('err', err, 'response', response)
})</pre>
  </div>
  <div class="tab-pane" id="csharp104">
<pre>
Console.Write("Zone ID: \n");
int zoneID = Convert.ToInt32(Console.ReadLine());

api.Delete("/clients/{id}/zones/pull/" + zoneID + "/zoneshields.json");
</pre>
  </div>
  <div class="tab-pane" id="response104">
    <pre>
{
  "code": 200
}</pre>
  </div>
</div>
