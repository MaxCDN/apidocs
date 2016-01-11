# Account API

## Get Account

Gets account information

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients/{id}/account.json</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | Account ID |
`name` | The name of your account |
`address_id` | Address ID |
`alias` | Company Alias |
`ssl_credits` | SSL Credits |
`flex_credits` | Flex Location Credits |
`date_created` | Date Created |
`date_updated` | Date Updated |

### Code Samples

<ul class="nav nav-tabs" id="myTab1">
  <li class="active"><a href="#ruby1" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python1" data-toggle='tab'>Python</a></li>
  <li><a href="#perl1" data-toggle='tab'>Perl</a></li>
  <li><a href="#php1" data-toggle='tab'>PHP</a></li>
  <li><a href="#node1" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp1" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#java1" data-toggle='tab'>Java</a></li>
  <li><a href="#response1" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby1">
<pre>
api.get("/clients/{id}/account.json")</pre>
  </div>
  <div class="tab-pane" id="python1">
<pre>api.get("/clients/{id}/account.json")</pre>
  </div>
    <div class="tab-pane" id="perl1">
<pre>my $data = $api->get("/clients/{id}/account.json");
print $data->{'account'}{'name'};</pre>
  </div>
  <div class="tab-pane" id="php1">
<pre>
$api->get('/clients/{id}/account.json');</pre>
  </div>
  <div class="tab-pane" id="node1">
  <pre>
api.get('/account.json', callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
    <div class="tab-pane" id="csharp1">
<pre>
api.Get("/clients/{id}/account.json");
</pre>
  </div>
      <div class="tab-pane" id="java1">
  <pre>
MaxCDNObject response = api.get("/clients/{id}/account.json");
Console.log(response.error ? "Error " + response.getErrorMessage()  : response.code);</pre>
    </div>
  <div class="tab-pane" id="response1">
    <pre>
{
    "code": 200,
    "data": {
        "account": {
            "alias": "aliasname",
            "date_created": "2013-05-15 17:32:30",
            "date_updated": "2013-05-15 19:43:36",
            "edgerules_credits": "0",
            "flex_credits": "-1",
            "id": "#####",
            "name": "MaxCDN sampleCode",
            "secure_token_pull_credits": "0",
            "server_id": "18",
            "ssl_credits": "1",
            "status": "2",
            "storage_quota": "107374182400",
            "storage_server_id": "11",
            "zone_credits": "-1"
        }
    }
}</pre>
  </div>
</div>


## Update Account

Updates account information

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients/{id}/account.json</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`name` | - | <span class="label important">required</span><br />length: 1-30 chars | The name of your account |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | Account ID |
`name` | The name of your account |
`address_id` | Address ID |
`alias` | Company Alias |
`ssl_credits` | SSL Credits |
`flex_credits` | Flex Location Credits |
`date_created` | Date Created |
`date_updated` | Date Updated |


### Code Samples

<ul class="nav nav-tabs" id="myTab2">
  <li class="active"><a href="#ruby2" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python2" data-toggle='tab'>Python</a></li>
  <li><a href="#perl2" data-toggle='tab'>Perl</a></li>
  <li><a href="#php2" data-toggle='tab'>PHP</a></li>
  <li><a href="#node2" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp2" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#java2" data-toggle='tab'>Java</a></li>
  <li><a href="#response2" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby2">
<pre>
params={"name"=> "UserName"}
api.put('/clients/{id}/account.json',params)</pre>
  </div>
  <div class="tab-pane" id="python2">
<pre>
params={"name": "Monty"}
api.put('/clients/{id}/account.json',params=params)</pre>
  </div>
    <div class="tab-pane" id="perl2">
<pre>
my @params = ('name=IDABIC');
$api->put("/clients/{id}/account.json", @params);</pre>
  </div>
  <div class="tab-pane" id="php2">
<pre>
$params = array("name"=>"newName");
$api->put('/clients/{id}/account.json',$params);</pre>
  </div>
  <div class="tab-pane" id="node2">
<pre>
api.put('/clients/{id}/account.json', { name: 'newName' }, callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
  <div class="tab-pane" id="csharp2">
<pre>
api.Put("/clients/{id}/account.json", "name=UserName");
</pre>
  </div>
    <div class="tab-pane" id="java2">
  <pre>
  MaxCDNRequest data = MaxCDN.newRequest("firstname", "Jane"); 
  MaxCDNObject response = api.put("/clients/{id}/account.json", data); 
  Console.log(response.error ? "Error " + response.getErrorMessage()  : response.code);</pre>
    </div>
  <div class="tab-pane" id="response2">
    <pre>
{
    "code": 200,
    "data": {
        "account": {
            "alias": "aliasname",
            "date_created": "2013-05-15 17:32:30",
            "date_updated": "2013-05-23 17:58:27",
            "edgerules_credits": "0",
            "flex_credits": "-1",
            "id": "#####",
            "name": "newName",
            "secure_token_pull_credits": "0",
            "server_id": "18",
            "ssl_credits": "-1",
            "status": "2",
            "storage_quota": "107374182400",
            "storage_server_id": "11",
            "zone_credits": "-1"
        }
    }
}</pre>
  </div>
</div>


## Get Account Address

Gets account address information

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients/{id}/account.json/address</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | Address ID |
`street1` | Street Address Line 1 |
`street2` | Street Address Line 2 |
`city` | City |
`state` | State |
`zip` | ZIP |
`country` | Country Code |
`date_created` | Date Created |
`date_updated` | Date Updated |


### Code Samples

<ul class="nav nav-tabs" id="myTab3">
  <li class="active"><a href="#ruby3" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python3" data-toggle='tab'>Python</a></li>
    <li><a href="#perl3" data-toggle='tab'>Perl</a></li>
  <li><a href="#php3" data-toggle='tab'>PHP</a></li>
  <li><a href="#node3" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp3" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#java3" data-toggle='tab'>Java</a></li>
  <li><a href="#response3" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby3">
<pre>
api.get('/clients/{id}/account.json/address')</pre>
  </div>
  <div class="tab-pane" id="python3">
<pre>
api.get('/clients/{id}/account.json/address')</pre>
  </div>
    <div class="tab-pane" id="perl3">
<pre>
my $data = $api->get("/clients/{id}/account.json/address");
print $data->{'address'}{'street1'};</pre>
  </div>
  <div class="tab-pane" id="php3">
<pre>
$api->get('/clients/{id}/account.json/address')</pre>
  </div>
  <div class="tab-pane" id="node3">
<pre>
api.get('/clients/{id}/account.json/address', callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
</div>
  <div class="tab-pane" id="csharp3">
<pre>
api.Get("/clients/{id}/account.json/address");
</pre>
</div>
  <div class="tab-pane" id="java3">
<pre>
String clientId = "222555";
MaxCDNObject response = api.get("/clients/{id}/clients/"+clientId+"/account.json/address");
Console.log(response.error ? "Error " + response.getErrorMessage()  : response.code);</pre>
</div>
  <div class="tab-pane" id="response3">
    <pre>
{
    "code": 200,
    "data": {
        "address": {
            "city": "los angeles",
            "country": "US",
            "date_created": "0000-00-00 00:00:00",
            "date_updated": "2013-05-15 19:54:40",
            "id": "#####",
            "state": "CA",
            "street1": "123 Main Street",
            "street2": "apt 42",
            "zip": "90068"
        }
    }
}
</pre>
  </div>
</div>


## Update Account Address

Updates account address information

<div class="heading">
<div class="url PUT"><span class="http_method">PUT</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients/{id}/account.json/address</span></div>
</div>

### Accepted Request Parameters

Parameter | Default Value | Validation | Description |
--- | --- | --- | --- | ---
`street1` | - | length: 1-200 chars | Street Address Line 1 |
`street2` | - | length: 1-200 chars | Street Address Line 2 |
`city` | - | length: 1-50 chars | City |
`state` | - | length: 1-50 chars | State |
`zip` | - | length: 3-5 chars; only digits accepted | ZIP |
`country` | - | length: 2 chars | Country Code |


### Response Parameters

Parameter | Description |
--- | --- | ---
`id` | Address ID |
`street1` | Street Address Line 1 |
`street2` | Street Address Line 2 |
`city` | City |
`state` | State |
`zip` | ZIP |
`country` | Country Code |
`date_created` | Date Created |
`date_updated` | Date Updated |


### Code Samples

<ul class="nav nav-tabs" id="myTab4">
  <li class="active"><a href="#ruby4" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python4" data-toggle='tab'>Python</a></li>
  <li><a href="#perl4" data-toggle='tab'>Perl</a></li>
  <li><a href="#php4" data-toggle='tab'>PHP</a></li>
  <li><a href="#node4" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp4" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#java4" data-toggle='tab'>Java</a></li>
  <li><a href="#response4" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby4">
<pre>
params = {"street1"=> "1234 Main Street", "street2"=> "apt 42", "state"=> "CA"}
api.put('/clients/{id}/account.json/address',params)</pre>
  </div>
  <div class="tab-pane" id="python4">
<pre>
params = {"street1": "1234 Main Street", "street2": "apt 42", "state": "CA"}
api.put('/clients/{id}/account.json/address',params=params)</pre>
  </div>
    <div class="tab-pane" id="perl4">
<pre>
my @params = ('street1=Main');
$api->put("/clients/{id}/account.json/address", @params);</pre>
  </div>
  <div class="tab-pane" id="php4">
<pre>
$params = array("street1"=>"123 Main Street", "street2"=>"apt 42", "state"=>"CA");
$api->put('/clients/{id}/account.json/address',$params);</pre>
  </div>
  <div class="tab-pane" id="node4">
<pre>
api.put('/clients/{id}/account.json/address', { street1: '123 Main Street', street2: 'apt 42', state: 'CA' }, callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
  <div class="tab-pane" id="csharp4">
<pre>
api.Put("/clients/{id}/account.json/address", "street1=1234 Main Street");
</pre>
  </div>
    <div class="tab-pane" id="java4">
  <pre>
MaxCDNRequest data = MaxCDN.newRequest("street1", "Main St 12").append("street2", "Lake St 13"); 
MaxCDNObject response = api.put("/clients/{id}/clients/"+clientId+"/account.json/address", data); 
Console.log(response.error ? "Error " + response.getErrorMessage()  : response.code);</pre>
    </div> 
  <div class="tab-pane" id="response4">
    <pre>
{
    "code": 200,
    "data": {
        "address": {
            "city": "los angeles",
            "country": "US",
            "date_created": "0000-00-00 00:00:00",
            "date_updated": "2013-05-23 18:01:29",
            "id": "#####",
            "state": "CA",
            "street1": "1234 Main Street",
            "street2": "apt 42",
            "zip": "90068"
        }
    }
}</pre>
  </div>
</div>



