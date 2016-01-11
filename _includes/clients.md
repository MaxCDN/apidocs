<h2>Clients API - Resellers Specific</h2>

## List Clients

Returns a list of all users on the specified account

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients.json</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`email` | Email Address |
`firstname` | First Name |
`lastname` | Last Name |
`phone` | Phone Number |
`name` | Name of the Company |
`companyalias` | Alias of the Company |
`group_id` | Group ID Number |
`address1` | Address, first line |
`city` | City |
`state` | State |
`postcode` | City Post/ZIP Code |
`country` | Country |
`password` | Password |
`active` | Whether or not the client is active |

### Code Samples

<ul class="nav nav-tabs" id="myTab5">
  <li class="active"><a href="#ruby205-0" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python205-0" data-toggle='tab'>Python</a></li>
  <li><a href="#perl205-0" data-toggle='tab'>Perl</a></li>
  <li><a href="#php205-0" data-toggle='tab'>PHP</a></li>
  <li><a href="#node205-0" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp205-0" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#java205-0" data-toggle='tab'>Java</a></li>
  <li><a href="#response205-0" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby205-0">
<pre>
api.get('/clients.json')</pre>
  </div>
  <div class="tab-pane" id="python205-0">
    <pre>
api.get('/clients.json')</pre>
  </div>
    <div class="tab-pane" id="perl205-0">
<pre>
my $data = $api->get("/clients.json");
print $data->{'users'}[0]{'id'};</pre>
  </div>
  <div class="tab-pane" id="php205-0">
<pre>
$api->get('/clients.json');</pre>
  </div>
  <div class="tab-pane" id="node205-0">
<pre>
api.get('/clients.json', callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
  <div class="tab-pane" id="csharp205-0">
<pre>
api.Get("/clients.json");
</pre>
  </div>
    <div class="tab-pane" id="java205-0">
  <pre>
MaxCDNObject response = api.get('/clients.json');
Console.log(response.error ? "Error " + response.getErrorMessage()  : response.code);
  </pre>
    </div>
  <div class="tab-pane" id="response205-0">
    <pre>
{
            "code": 201,
            "data": {
                "Client": {
                    "group_id": null,
                    "company_id": "Company Name",
                    "company_alias": "Company Alias"
                    "date_created": "2013-05-23 18:22:11",
                    "status": "Active",
                    "date_last_login": null,
                    "date_updated": null,
                    "default_company_id": "19538",
                    "email": "name@domain.com",
                    "firstname": "Given",
                    "ip_last_login": null,
                    "isdisabled": 0,
                    "lastname": "Family",
                    "phone": null,
                    "timezone": "America/Los_Angeles"
                }
            }
        }</pre>
  </div>
</div>

## Create Client

Creates a new client on the specified account

<div class="heading">
<div class="url POST"><span class="http_method">POST</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients.json</span></div>
</div>

### Accepted Request Parameters
<table>
<th>Parameter</th><th>Default Value</th><th>Validation</th><th>Description</th>

<tr>
	<td>name</td>
	<td> - </td>
	<td><span class="label important">required</span><br />length: 1-255 chars</td>
	<td>Company Name</td>
</tr>
<tr>
	<td>alias</td>
	<td> - </td>
	<td><span class="label important">required</span><br />length: 1-45 chars</td>
	<td>Company Alias</td>
</tr>
<tr>
	<td>package_id</td>
	<td> - </td>
	<td><span class="label important">required</span><br /> length: 1-11 chars</td>
	<td>Package ID Number (Contact your sales representative to determine your Package ID Number)</td>
</tr>
<tr>
	<td>account_owner</td>
	<td> - </td>
	<td><span class="label important">required</span><br /> A JSON Encoded Array including 'email', 'firstname', 'lastname', 'password', 'phone'</td>
	<td>
		Account Owner Information:
		<br/>
		<br/>
		<ul>
			<li>'email' - Account Owner's Email</li>
			<li>'firstname' - Account Owner's First Name</li>
			<li>'lastname' - Account Owner's Last Name</li>
			<li>'password' - Account's Password</li>
			<li>'phone' - Account Owner's Phone Number</li>
		</ul>

	</td>
</tr>
<tr>
	<td>address</td>
	<td> - </td>
	<td><span class="label important">required</span><br /> A JSON Encoded Array including street1, street2 (not required), City, State, ZIP / Postal Code, Country</td>
	<td>Account Owner Address</td>
</tr>
<tr>
	<td>paymentmethod</td>
	<td>'mailin'</td>
	<td><span class="label important">required</span><br /></td>
	<td>Payment Method "Hard code this to Mail-In Payment"</td>
</tr>
<tr>
	<td>generateinvoice</td>
	<td>'0'</td>
	<td><span class="label important">required</span><br /></td>
	<td>Hard Code this to not generate an invoice with the parameter '0'</td>
</tr>

</table>

### Response Parameters

Parameter | Description |
--- | --- | ---
`email` | Email Address |
`firstname` | First Name |
`lastname` | Last Name |
`phone` | Phone Number |
`name` | Name of the Company |
`alias` | Alias of the Company |
`group_id` | Group ID Number |
`address1` | Address, first line |
`city` | City |
`state` | State |
`postcode` | City Post/ZIP Code |
`country` | Country |
`password` | Password |
`active` | Whether or not the client is active |

### Code Samples

<ul class="nav nav-tabs" id="myTab1">
  <li class="active"><a href="#ruby205" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python205" data-toggle='tab'>Python</a></li>
  <li><a href="#perl205" data-toggle='tab'>Perl</a></li>
  <li><a href="#php205" data-toggle='tab'>PHP</a></li>
  <li><a href="#node205" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp205" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#java205" data-toggle='tab'>Java</a></li>
  <li><a href="#response205" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby205">
    <pre>
account_owner={
            "firstname"=>"First Name",
            "lastname"=>"Last Name",
            "email"=>"E-Mail",
            "phone"=>"1234567890",
            "password"=>"password"
        }

        address={
            "street1"=>"Street One",
            "street2"=>"Not Required",
            "city"=>"City Name",
            "state"=>"State",
            "zip"=>"ZIP / Postal Code",
            "country"=>"US (or country name)"
        }

        params={
            "name"=>"Company Name",
            "alias"=>"Company Alias",
            "package_id"=>"x",
            "account_owner"=>account_owner.to_json,
            "address"=>address.to_json,
            "paymentmethod"=>"mailin"
        }

        api.post('/clients.json',params)</pre>
  </div>
  <div class="tab-pane" id="python205">
    <pre>account_owner = {
            'firstname':'First Name',
            'lastname':'Last Name',
            'email':'E-Mail',
            'phone':'1234567890',
            'password':'password'
        }

        address = {
            'street1':'Street One',
            'street2':'Not Required',
            'city':'City Name',
            'state':'State',
            'zip':'ZIP / Postal Code',
            'country':'US (or country name)'
        }

        params = {
            'name":'Company Name',
            'alias':'Company Alias',
            'group_id':'Group ID',
            'package_id':'x',
            'account_owner':json.dumps(account_owner),
            'address':json.dumps(address),
            'paymentmethod':'mailin'
        }

        api.post('/clients.json',data=params)</pre>
  </div>
    <div class="tab-pane" id="perl205">
    <pre>my @account_owner = {
            "firstname"=>"First Name",
            "lastname"=>"Last Name",
            "email"=>"E-Mail",
            "phone"=>"1234567890",
            "password"=>"password"
        }

        my @address = {
            "street1"=>"Street One",
            "street2"=>"Not Required",
            "city"=>"City Name",
            "state"=>"State",
            "zip"=>"ZIP / Postal Code",
            "country"=>"US (or country name)"
        }

        my @params = {
            "name"=>"Company Name",
            "alias"=>"Company Alias",
            "group_id"=>"Group ID",
            "package_id"=>"x",
            "account_owner"=>encode_json(\@account_owner),
            "address"=>encode_json(\@address),
            "paymentmethod"=>"mailin"
        }

    my $data = $api->post("/clients.json", @params);</pre>
  </div>
  <div class="tab-pane" id="php205">
    <pre>
$account_owner = array(
            'firstname' => 'john',
            'lastname'  => 'doe',
            'email'     => 'johndoe@gmail.com',
            'phone'     => '555-555-5555',
            'password'  => 'testpass'
        );


        $address = array(
            'street1' => '123 Fake St.',
            'city'    => 'Los Angeles',
            'state'   => 'California',
            'zip'     => '90000',
            'country' => 'US'
        );

        $params = array(
            'name'          => 'New Account Name',
            'companyalias'         => 'newaccountalias',
            'group_id'      => '27',
            'package_id'    => 'x',
            'account_owner' => json_encode($account_owner),
            'address'       => json_encode($address)
            'paymentmethod' => 'mailin'
        );

        $response = $api->post("/clients.json", $params);</pre>
  </div>
  <div class="tab-pane" id="node205">
  <pre>
var account_owner = [
        firstname:'First Name',
        lastname:'Last Name',
        email:'E-Mail',
        phone:'1234567890',
        password:'password'
    ];

    var address = [
        street1: '123 Fake St.',
        city: 'Los Angeles',
        state: 'California',
        zip: '90000',
        country: 'US'
    ];

    var params = [
        name => 'New Account Name',
        companyalias => 'newaccountalias',
        group_id => '27',
        package_id => 'x',
        account_owner => json_encode(account_owner),
        address => json_encode(address),
        paymentmethod => 'mailin'
    ];

    api.post('/clients.json' + params, callback)
    function callback(err, response) {
      if (err) return console.log(err)
      console.log(response)
    }</pre>
  </div>
    <div class="tab-pane" id="csharp205">
  <pre>var account_owner = [
        firstname:'First Name',
        lastname:'Last Name',
        email:'E-Mail',
        phone:'1234567890',
        password:'password'
    ];
    var jsonSerializer = new System.Web.Script.Serialization.JavaScriptSerializer();
            string account_owner = jsonSerializer.Serialize(account_owner);
    var address = [
        street1: '123 Fake St.',
        city: 'Los Angeles',
        state: 'California',
        zip: '90000',
        country: 'US'
    ];
    var jsonSerializer = new System.Web.Script.Serialization.JavaScriptSerializer();
            string address = jsonSerializer.Serialize(address);
    var params = [
        name => 'New Account Name',
        companyalias => 'newaccountalias',
        group_id => '27',
        package_id => 'x',
        account_owner => account_owner,
        address => address,
        paymentmethod => 'mailin'
    ];

api.Post("/clients.json", params);
</pre>
  </div>
      <div class="tab-pane" id="java205">
    <pre>
	    account_owner = {
	                'firstname':'First Name',
	                'lastname':'Last Name',
	                'email':'E-Mail',
	                'phone':'1234567890', 
	                'password':'password' 
	            }
            
	            address = {
	                'street1':'Street One',
	                'street2':'Not Required',
	                'city':'City Name',
	                'state':'State', 
	                'zip':'ZIP / Postal Code', 
	                'country':'US (or country name)'
	            }
            
	            params = {
	                'name":'Company Name',
	                'alias':'Company Alias',
	                'group_id':'Group ID',
	                'package_id':'x', 
	                'account_owner':json.dumps(account_owner), 
	                'address':json.dumps(address),
	                'paymentmethod':'mailin'
	            }
            
	            api.post('/clients.json',data=params);
				
				String firstname = "First Name";
				String lastname = "Last Name";
				String email = "E-Mail";
				String phone = "1234567890"; 
				String password = "password"; 
				String account_owner[] = { "firstname", "lastname", "email", "phone", "password"};
				JSONArray saccount_owner = new JSONArray(Arrays.asList(account_owner));

				String street1 = "Street One";
				String street2 = "Not required";
				String city = "Citu name";
				String state = "State"; 
				String zip = "6902"; 
				String country = "US";
				String address[] = { "street1", "street2", "city", "state", "zip", "country"};
				JSONArray saddress = new JSONArray(Arrays.asList(address));

				MaxCDNRequest data = MaxCDN.newRequest("name", "Company Name").append("alias", "Company alias").append("group_id", "Group ID").append("package_id", "x").append("account_owner", "saccount_owner").append("address", "saddress").append("paymentmethod", "mailin");
				MaxCDNObject response = api.post("/clients.json", data);
				Console.log(response.error ? "Error " + response.getErrorMessage()  : response.code);
				
				
  </pre>
    </div>
  <div class="tab-pane" id="response205">
    <pre>{"code"=>201,
 "data"=>
  {"account"=>
    {"id"=>50353,
     "name"=>"maxsupporttest5",
     "address_id"=>49941,
     "alias"=>"maxsupporttest5",
     "date_created"=>"2015-10-27 18:23:39",
     "date_updated"=>nil,
     "brand_id"=>"38",
     "whmcs_client_id"=>57820,
     "package_id"=>"310",
     "parent_id"=>"5032",
     "status"=>2,
     "notify_bw"=>0,
     "storage_quota"=>"107374182400",
     "ssl_credits"=>-1,
     "flex_credits"=>0,
     "enable_wwwcname"=>0,
     "enable_starcname"=>0,
     "enable_rules"=>0,
     "enable_devtools"=>0,
     "query_strings"=>2,
     "zone_credits"=>-1,
     "secure_token_pull_credits"=>0,
     "rawlog_export_credits"=>0,
     "zoneshield_credits"=>0,
     "edgerules_credits"=>0,
     "default_pull_zone_ip_id"=>"10951",
     "default_push_zone_ip_id"=>"11280",
     "default_storage_ip_id"=>"11312",
     "default_vod_storage_ip_id"=>"10985",
     "default_vod_rtmp_ip_id"=>"10986",
     "default_vod_direct_ip_id"=>"10986",
     "default_vod_pseudo_ip_id"=>"10987",
     "maintain_scheme"=>0,
     "v2_provisioning"=>0}}}</pre>
  </div>
</div>

<div id="reseller-create-user"></div>

## Get Client Bandwidth

Gets client bandwidth information

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients/{id}/bandwidth.json</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`valid_until` | Date bandwidth expires |
`credit` | Bandwidth Credit |
`still_valid` | Extended Bandwidth Life Validation |
`base` | Base Bandwidth Ammount |
`expiration` | Bandwidth Expiration |
`purchased` | Date Bandwidth Was Purchased |

### Code Samples

<ul class="nav nav-tabs" id="myTab1">
  <li class="active"><a href="#ruby200" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python200" data-toggle='tab'>Python</a></li>
  <li><a href="#perl200" data-toggle='tab'>Perl</a></li>
  <li><a href="#php200" data-toggle='tab'>PHP</a></li>
  <li><a href="#node200" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp200" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#java200" data-toggle='tab'>Java</a></li>
  <li><a href="#response200" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby200">
    <pre>
api.get("/clients/{id}/bandwidth.json")</pre>
  </div>
  <div class="tab-pane" id="python200">
    <pre>api.get("/clients/{id}/bandwidth.json")</pre>
  </div>
    <div class="tab-pane" id="perl200">
    <pre>my $data = $api->get("/clients/{id}/bandwidth.json");</pre>
  </div>
  <div class="tab-pane" id="php200">
    <pre>
$api->get('/clients/{id}/bandwidth.json');</pre>
  </div>
  <div class="tab-pane" id="node200">
  <pre>
api.get('/clients/{id}/bandwidth.json', callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
    <div class="tab-pane" id="csharp200">
  <pre>
api.Get("/clients/{id}/bandwidth.json");
</pre>
  </div>
      <div class="tab-pane" id="java200">
    <pre>
MaxCDNObject response = api.get("/clients/{id}/bandwidth.json");
Console.log(response.error ? "Error " + response.getErrorMessage()  : response.code);
  </pre>
    </div>
  <div class="tab-pane" id="response200">
    <pre>
{
    "code": 200,
    "data": {
        "account": {total": "1",
        "summary": [{
            "valid_until": "Jun 07, 2011",
            "credit": "10",
            "still_valid": false,
            "base": 1000,
            "expiration": false,
            "purchased": "Jun 07, 2010", "debit": 11107173020
            }]
        }
    }
}</pre>
  </div>
</div>

## Get Storage Data

Gets relevant storage data

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients/{id}/storage.json</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`zone_id` | Zone ID |
`storage` | Amount of Storage Used |
`storage_id ` | Storage ID |
`zone_type` | Type of Zone |
`zone_name` | Name of Zone |
`last_updated` | Date Last Updated |

### Code Samples

<ul class="nav nav-tabs" id="myTab1">
  <li class="active"><a href="#ruby201" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python201" data-toggle='tab'>Python</a></li>
  <li><a href="#perl201" data-toggle='tab'>Perl</a></li>
  <li><a href="#php201" data-toggle='tab'>PHP</a></li>
  <li><a href="#node201" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp201" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#java201" data-toggle='tab'>Java</a></li>
  <li><a href="#response201" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby201">
    <pre>
api.get("/clients/{id}/storage.json")</pre>
  </div>
  <div class="tab-pane" id="python201">
    <pre>api.get("/clients/{id}/storage.json")</pre>
  </div>
    <div class="tab-pane" id="perl201">
    <pre>my $data = $api->get("/clients/{id}/storage.json");</pre>
  </div>
  <div class="tab-pane" id="php201">
    <pre>
api->get('/clients/{id}/storage.json');</pre>
  </div>
  <div class="tab-pane" id="node201">
  <pre>
api.get('/clients/{id}/storage.json', callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
    <div class="tab-pane" id="csharp201">
  <pre>
api.Get("/clients/{id}/storage.json");
</pre>
  </div>
   <div class="tab-pane" id="java201">
    <pre>
MaxCDNObject response = api.get("/clients/{id}/storage.json");
Console.log(response.error ? "Error " + response.getErrorMessage()  : response.code);
  </pre>
    </div>
  <div class="tab-pane" id="response201">
    <pre>
{
    "code": 200, "data": {
        "stats": [
        {
            "last_updated": "2014-11-13 18:39:19",
            "zone_id": "{zoneid}",
            "storage_used": "1234",
            "storage_id": "1",
            "zone_type": "1",
            "zone_name": "zonename"},
        {
            "last_updated": "2014-11-13 16:00:50",
            "zone_id": "zoneid",
            "storage_used": "5678",
            "storage_id": "2",
            "zone_type": "2",
            "zone_name": "zonename2"
        },
        {
            "last_updated": "2014-11-13 16:00:08",
            "zone_id": "zoneid",
            "storage_used": "9012",
            "storage_id": "3",
            "zone_type": "3",
            "zone_name": "zonename3"
        },
        {
            "last_updated": "2014-11-13 18:39:19",
            "zone_id": "zoneid",
            "storage_used": "3456",
            "storage_id": "4",
            "zone_type": "4",
            "zone_name": "zonename4"
        },
        {
            "last_updated": "2014-11-13 16:00:50",
            "zone_id": "zoneid",
            "storage_used": "7890",
            "storage_id": "5",
            "zone_type": "5",
            "zone_name": "zonename"}
        ],
    "page_size": "50",
    "pages": 1,
    "current_page_size": 1,
    "total": "1",
    "page": 1
    }
}</pre>
  </div>
</div>

## Get Storage Used

Gets the amount of storage that has currently been used.

<div class="heading">
<div class="url GET"><span class="http_method">GET</span>
<span class="path">https://rws.maxcdn.com/{companyalias}/clients/{id}/storage/used.json</span></div>
</div>

### Response Parameters

Parameter | Description |
--- | --- | ---
`storage` | Storage Amount |

### Code Samples

<ul class="nav nav-tabs" id="myTab1">
  <li class="active"><a href="#ruby202" data-toggle='tab'>Ruby</a></li>
  <li><a href="#python202" data-toggle='tab'>Python</a></li>
  <li><a href="#perl202" data-toggle='tab'>Perl</a></li>
  <li><a href="#php202" data-toggle='tab'>PHP</a></li>
  <li><a href="#node202" data-toggle='tab'>Node</a></li>
  <li><a href="#csharp202" data-toggle='tab'>.NET/C#</a></li>
  <li><a href="#java202" data-toggle='tab'>Java</a></li>
  <li><a href="#response202" data-toggle='tab'>Response</a></li>
</ul>

<div class="tab-content">
  <div class="tab-pane active" id="ruby202">
    <pre>
api.get("/clients/{id}/storage/used.json")</pre>
  </div>
  <div class="tab-pane" id="python202">
    <pre>api.get("/clients/{id}/storage/used.json")</pre>
  </div>
    <div class="tab-pane" id="perl202">
    <pre>my $data = $api->get("/clients/{id}/storage/used.json");</pre>
  </div>
  <div class="tab-pane" id="php202">
    <pre>
api->get('/clients/{id}/storage/used.json');</pre>
  </div>
  <div class="tab-pane" id="node202">
  <pre>
api.get('/clients/{id}/storage/used.json', callback)
function callback(err, response) {
  if (err) return console.log(err)
  console.log(response)
}</pre>
  </div>
    <div class="tab-pane" id="csharp202">
  <pre>
api.Get("/clients/{id}/storage/used.json");
</pre>
  </div>
      <div class="tab-pane" id="java202">
    <pre>
MaxCDNObject response = api.get("/clients/{id}/storage/used.json");
Console.log(response.error ? "Error " + response.getErrorMessage()  : response.code);
  </pre>
    </div>
  <div class="tab-pane" id="response202">
    <pre>
{
"code": 200,
"data": {
    "storage": "1535815680"
    }
}</pre>
  </div>
</div>

<div id="reseller-account-api"></div>
